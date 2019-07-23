---
ID: 36
post_title: >
  WordPress function execution order on a
  Page Load
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2017/02/wordpress-function-execution-order-on-a-page-load/
published: true
post_date: 2017-02-24 12:24:12
---
<h2>General</h2>
<pre>init();
parse_request($query_args);
send_headers();
query_posts();
handle_404();
register_globals();</pre>
<h2>do_action calls are made in the following order</h2>
<pre>muplugins_loaded
 registered_taxonomy
 registered_taxonomy
 registered_taxonomy
 registered_taxonomy
 registered_taxonomy
 registered_post_type
 registered_post_type
 registered_post_type
 registered_post_type
 registered_post_type
 plugins_loaded
 sanitize_comment_cookies
 setup_theme
 unload_textdomain
 load_textdomain
 after_setup_theme
 load_textdomain
 load_textdomain
 auth_cookie_malformed
 auth_cookie_valid
 set_current_user
 init
 registered_post_type
 registered_post_type
 registered_post_type
 registered_post_type
 registered_post_type
 registered_taxonomy
 registered_taxonomy
 registered_taxonomy
 registered_taxonomy
 registered_taxonomy
 widgets_init
 register_sidebar
 register_sidebar
 register_sidebar
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_register_sidebar_widget
 wp_loaded
 parse_tax_query
 parse_tax_query
 posts_selection
 template_redirect
 admin_bar_init
 add_admin_bar_menus
 get_header
 wp_head
 wp_enqueue_scripts
 wp_print_styles
 wp_print_scripts
 get_template_part_content
 begin_fetch_post_thumbnail_html
 end_fetch_post_thumbnail_html
 get_template_part_content
 get_template_part_content
 get_template_part_content
 get_template_part_content
 get_template_part_content
 get_template_part_content
 get_template_part_content
 get_template_part_content
 get_template_part_content
 begin_fetch_post_thumbnail_html
 end_fetch_post_thumbnail_html
 get_sidebar
 dynamic_sidebar_before
 dynamic_sidebar
 dynamic_sidebar_after
 get_footer
 twentytwelve_credits
 wp_footer
 wp_print_footer_scripts
 wp_before_admin_bar_render
 wp_after_admin_bar_render
 shutdown</pre>
&nbsp;