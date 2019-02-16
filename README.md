# alux-nav-walker
This is a custom nav walker menù for wordpress based on Alux framework 


Add this code on functions.php

/* Register Custom Navigation Walker
---------------------------------------------------------*/
require_once('assets/alux-nav-walker.php');


On header display navigation menu

wp_nav_menu([
     'menu'             => 'header',
     'theme_location'  => 'header',
     'container'       => 'nav',
     'container_id'    => 'menu-sub-2',
     'container_class' => 'nav-container',
     'menu_id'         => false,
     'menu_class'      => 'primary',
     'depth'           => 0,
     'fallback_cb'     => 'alux_nav_walker::fallback',
     'walker'          => new alux_nav_walker()
    ]);
