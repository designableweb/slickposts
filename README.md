<h1>Slick Posts Slider</h1>
<p>WordPress plugin that allows users to display a slick.js slider. It's a simple plugin that leverages the Slick slider to display a carousel of posts.</p>

<h2>Features</h2>
Enqueue necessary Slick.js files
Defines a custom shortcode [slick_posts_slider] to display a slider with posts
You can specify the post type with the post_type attribute in the shortcode. Default post type is 'post'

<h2>Requirements</h2>
This plugin requires the following JavaScript and CSS files from Slick Slider:

slick.min.js
slick.css
slick-theme.css
These files should be downloaded and placed within the plugin folder in folders named "js" and "css".

Slick Slider assets can be downloaded from the <a href="https://github.com/kenwheeler/slick/">Slick GitHub repository</a>

<h2>Installation</h2>
<ul>
<li>Download the zip file and extract the contents into a folder named "slick-posts-slider".</li>
<li>Download the necessary <a href="https://github.com/kenwheeler/slick/">Slick Slider assets</a> and place them in the css and js folders within the slick-posts-slider folder.</li>
<li>Upload the slick-posts-slider folder to your /wp-content/plugins/ directory.</li>
<li>Activate the Slick Posts Slider plugin through the 'Plugins' menu in WordPress.</li>
</ul>
  
<h2>Usage</h2>
Place the [slick_posts_slider] shortcode wherever you want the posts slider to appear.

Example: [slick_posts_slider post_type='your_post_type']

<h2>How do I use the shortcode?</h2>
Place the [slick_posts_slider] shortcode wherever you want the posts slider to appear.

<h2>Can I display other post types besides 'post'</h2>
Yes, you can specify the post type with the post_type attribute in the shortcode.

<strong>Changelog</strong>
1.0 Initial release
