---
ID: 827
post_title: 'SSH : Change Owner of files and folders'
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2017/07/ssh-change-owner-files-folders/
published: true
post_date: 2017-07-20 13:27:45
---
<h2>Change Owner of All files within a Folder</h2>
Here is how to change Owner of Files and Folders in SSH as a Bulk
<ul>
 	<li>Login to SSH</li>
 	<li>Run
<pre>chown -R user:usergroup /location/of/the/folder/*</pre>
</li>
</ul>
<h2>Change Owner of one file</h2>
<pre>chown user:usergroup /location/of/the/folder/file-name.php</pre>
<h2>Find the list of files under a Owner</h2>
<pre>find /location/of/the/folder/ -user USERNAME</pre>