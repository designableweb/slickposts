<?php
/*
Plugin Name: Slick Posts Slider
Description: Allows users to display a slick.js slider using a shortcode
Version: 1.0
Author: Your Name
*/

function slick_posts_slider_enqueue_scripts() {
    wp_enqueue_style( 'slick', plugin_dir_url( __FILE__ ) . 'css/slick.css', array(), '1.8.1' );
    wp_enqueue_style( 'slick-theme', plugin_dir_url( __FILE__ ) . 'css/slick-theme.css', array(), '1.8.1' );
    wp_enqueue_script( 'slick', plugin_dir_url( __FILE__ ) . 'js/slick.min.js', array( 'jquery' ), '1.8.1', true );
    wp_enqueue_script( 'slick-init', plugin_dir_url( __FILE__ ) . 'js/slick-init.js', array( 'slick' ), '1.0', true );
}

add_action( 'wp_enqueue_scripts', 'slick_posts_slider_enqueue_scripts' );

function slick_posts_slider_shortcode($atts) {
    $atts = shortcode_atts( array(
        'post_type' => 'post',
    ), $atts );

    $args = array(
        'post_type' => $atts['post_type'],
        'post_status' => 'publish',
        'posts_per_page' => 6,
        'orderby' => 'date',
        'order' => 'DESC',
    );
    
    $query = new WP_Query($args);
    $output = '<div class="single-item-slider">';

    if ($query->have_posts()) {
        while ($query->have_posts()) {
            $query->the_post();
            $post_link = esc_url(get_permalink());
            $post_title = esc_html(get_the_title());
            $post_image = esc_url(get_the_post_thumbnail_url());
            $output .= '<div>';
            $output .= '<a href="' . $post_link . '">';
            $output .= '<img src="' . $post_image . '" alt="' . $post_title . '">';
            $output .= '<h2>' . $post_title . '</h2>';
            $output .= '</a>';
            $output .= '</div>';
        }
    }
    wp_reset_postdata();

    $output .= '</div>';
    
    return $output;
}

add_shortcode( 'slick_posts_slider', 'slick_posts_slider_shortcode' );
