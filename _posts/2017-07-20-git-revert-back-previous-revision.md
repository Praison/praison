---
ID: 832
post_title: 'Git : Revert back to Previous Revision'
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2017/07/git-revert-back-previous-revision/
published: true
post_date: 2017-07-20 13:57:56
---
<h2>Revert back to Previous version in git</h2>
<h3>Required</h3>
<ul>
 	<li>Get the REVISIONNUMBER ( Revision number ) of the previous Revision which you want the files to revert back to.</li>
</ul>
Here is how you could revert back to previous Revision in git
<ol>
 	<li>git reset --hard REVISIONNUMBER</li>
 	<li>git push --force</li>
</ol>
<h3>Caution</h3>
This will delete all yours commits made between the REVISIONNUMBER and the CURRENT Revisionnumber