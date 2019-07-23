---
ID: 739
post_title: GitIgnore Directory
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2017/03/gitignore-directory/
published: true
post_date: 2017-03-28 09:28:37
---
.gitignore Directory

Example Directory name : uploads
<h2>Ignoring ALL folders and files</h2>
<pre> # .gitignore
uploads
</pre>
<strong>Result:</strong>
<pre># Will Ignore

/uploads # directory
/uploads # file
/example/path/uploads # directory
/example/path/uploads # file
</pre>
<h2 id="what-if-you-just-want-to-ignore-the-directory-at-the-root-level">Ignoring only the Root Directory</h2>
The correct syntax for that is to put leading and trailing slash:
<pre> # .gitignore
/uploads/
</pre>
<strong>Result:</strong>
<pre> # will ignore
/uploads # directory

# will NOT ignore
/uploads              # file
/some/path/uploads    # directory
/another/path/uploads # file
</pre>
<h2>Ignoring only the Root Directory and the Root File</h2>
<pre> # .gitignore
/uploads</pre>
<strong>Result:</strong>
<pre># will ignore

/uploads # directory
/uploads # file
</pre>
<h2>Ignoring only Folders and not Files</h2>
<pre># .gitignore
uploads/</pre>
<strong>Result:</strong>
<pre># will ignore:
/uploads # directory
/some/path/uploads # directory

# will NOT ignore:
/another/path/uploads # file</pre>