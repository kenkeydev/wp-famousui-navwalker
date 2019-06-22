# WP Famous UI NavWalker

Use the snippets below under **Get Started**


# Get Started

Put the following snippet into your themes functions.php

    register_nav_menu('header-menu',__( 'Header Menu' ));


Use the following snippet to display the menu anywhere in the theme

    <?
    require_once get_template_directory() . '/class-wp-famousui-navwalker.php';
    wp_nav_menu( array(
      'theme_location'  => 'header-menu',
      'depth'	          => 3, // 1 = no dropdowns, 2 = with dropdowns.
      'container'       => '',
      'items_wrap' => '%3$s',
      'fallback_cb'     => 'WP_Famousui_Navwalker::fallback',
      'walker'          => new WP_Famousui_Navwalker(),
    ) );
    ?>
