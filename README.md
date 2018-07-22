# BWWalker

A custom subclass of Wordpress' Walker_Nav_Menu class that helps developers to use Bootstrap 4 navbar inside Wordpress.


This class was created using the Wordpress 4.9.7 & Bootstrap 4.1.2.

A sample code:


        <nav class="navbar navbar-expand-lg navbar-light navbar-expand-lg jz-shadow fixed-top" style="background-color: #f4d042">
          <a class="navbar-brand" href="<?php bloginfo('url');?>"><?php bloginfo('name');?></a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>

          <div class="collapse navbar-collapse" id="navbarNav">

          <?php
            wp_nav_menu(
              array(
                'theme_location'  =>    'primary',
                'menu_class'      =>    'navbar-nav mr-auto mt-2 mt-lg-0',
                'container'       =>    false,
                'walker'          =>    new BWWalker()
              )
            );
          ?>
            <?php get_search_form();?> <!-- You can use a search form here using Bootstrap 4 inline search form -->
          </div>
        </nav>        
 
