Slick Posts Slider
WordPress plugin that allows users to display a slick.js slider. It's a simple plugin that leverages the Slick slider to display a carousel of posts.

Features
Enqueue necessary Slick.js files
Defines a custom shortcode [slick_posts_slider] to display a slider with posts
You can specify the post type with the post_type attribute in the shortcode. Default post type is 'post'
Requirements
This plugin requires the following JavaScript and CSS files from Slick Slider:

slick.min.js
slick.css
slick-theme.css
These files should be downloaded and placed in the css and js folders within the plugin folder.

Slick Slider assets can be downloaded from the Slick GitHub repository: Slick

Installation
Download the zip file and extract the contents.
Download the necessary Slick Slider assets (links provided above) and place them in the css and js folders within the slick-posts-slider folder.
Upload the slick-posts-slider folder to your /wp-content/plugins/ directory.
Activate the Slick Posts Slider plugin through the 'Plugins' menu in WordPress.
Usage
Place the [slick_posts_slider] shortcode wherever you want the posts slider to appear.

Example: [slick_posts_slider post_type='your_post_type']

Frequently Asked Questions
How do I use the shortcode?
Place the [slick_posts_slider] shortcode wherever you want the posts slider to appear.

Can I display other post types besides 'post'?
Yes, you can specify the post type with the post_type attribute in the shortcode.

Changelog
1.0

Initial release
