---
ID: 521
post_title: Custom Fields in bbPress Topic Form
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2015/12/custom-fields-in-bbpress-topic-form/
published: true
post_date: 2015-12-11 12:13:42
---
<h2>Creating Fields</h2>
<pre>add_action ( 'bbp_theme_before_topic_form_content', 'bbp_extra_fields'); function bbp_extra_fields() { 

$value = get_post_meta( bbp_get_topic_id(), 'bbp_extra_field1', true); echo '&lt;label for="bbp_extra_field1"&gt;Extra Field 1&lt;/label&gt;&lt;br&gt;'; echo "&lt;input type='text' name='bbp_extra_field1' 

value='".$value."'&gt;"; $value = get_post_meta( bbp_get_topic_id(), 'bbp_extra_field2', true); echo '&lt;label for="bbp_extra_field1"&gt;Extra Field 2&lt;/label&gt;&lt;br&gt;'; echo "&lt;input type='text' name='bbp_extra_field2' value='".$value."'&gt;"; }

</pre>
<h2>Saving Custom Fields</h2>
<pre>add_action ( 'bbp_new_topic', 'bbp_save_extra_fields', 10, 1 ); add_action ( 'bbp_edit_topic', 'bbp_save_extra_fields', 10, 1 );

function bbp_save_extra_fields($topic_id=0) {

if (isset($_POST) &amp;&amp; $_POST['bbp_extra_field1']!='') update_post_meta( $topic_id, 'bbp_extra_field1', $_POST['bbp_extra_field1'] );

if (isset($_POST) &amp;&amp; $_POST['bbp_extra_field1']!='') update_post_meta( $topic_id, 'bbp_extra_field1', $_POST['bbp_extra_field2'] );

}</pre>
<h2>Displaying Fields on the Topic Page</h2>
<pre>add_action('bbp_template_before_replies_loop', 'bbp_show_extra_fields');

function bbp_show_extra_fields() {

$topic_id = bbp_get_topic_id();

$value1 = get_post_meta( $topic_id, 'bbp_extra_field1', true); 
$value2 = get_post_meta( $topic_id, 'bbp_extra_field2', true);

echo "Field 1: ".$value1."&lt;br&gt;"; 
echo "Field 2: ".$value2."&lt;br&gt;";

}</pre>