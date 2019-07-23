---
ID: 940
post_title: >
  Add Bootstrap to WordPress admin
  sub-menu page
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2018/01/add-bootstrap-to-wordpress-admin-sub-menu-page/
published: true
post_date: 2018-01-11 18:18:42
---
<h2>Add Bootstrap to a plugin page</h2>
<div></div>
<pre>// custom css and js
 add_action('admin_enqueue_scripts', 'cstm_css_and_js');

function cstm_css_and_js($hook) {
     // your-slug =&gt; The slug name to refer to this menu used in "add_submenu_page"
     // tools_page =&gt; refers to Tools top menu, so it's a Tools' sub-menu page
     if ( 'tools_page_your-slug' != $hook ) {
         return;
     }

    wp_enqueue_style('boot_css', plugins_url('inc/bootstrap.css',__FILE__ ));
     wp_enqueue_script('boot_js', plugins_url('inc/bootstrap.js',__FILE__ ));
 }</pre>