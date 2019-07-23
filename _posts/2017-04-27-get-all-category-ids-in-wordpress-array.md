---
ID: 754
post_title: 'Get all category ids in WordPress [Array]'
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2017/04/get-all-category-ids-in-wordpress-array/
published: true
post_date: 2017-04-27 11:32:44
---
Choose either one of these options to Get all category ids in WordPress as an Array
<h2>Get all category ids, Option 1</h2>
<pre>$output_categories = array();
$categories=get_categories($args);
 foreach($categories as $category) { 
 $output_categories[] = $category-&gt;cat_ID;
}</pre>
<h2>Get all category ids, Option 2</h2>
<pre>$categories_ids = get_terms(
 array( 'category' ), // Taxonomies
 array( 'fields' =&gt; 'ids' ) // Fields
);</pre>