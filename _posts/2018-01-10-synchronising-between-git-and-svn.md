---
ID: 928
post_title: Synchronising between Git and SVN
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2018/01/synchronising-between-git-and-svn/
published: true
post_date: 2018-01-10 09:37:20
---
Synchronizing updates between the two repositories.

1. Clone the GitHub Repo

SSH

<code>$ git clone git@github.com:Praison/seo-wordpress.git</code>

HTTPS

<code>$ git clone https://github.com/Praison/seo-wordpress.git</code>

2. Change into the Directory

<code>$ cd seo-wordpress</code>

3. Set Up a Subversion tracking branch
<pre>$ git branch --no-track svnsync 
$ git checkout svnsync
$ git svn init -s https://plugins.svn.wordpress.org/seo-wordpress/ --prefix=origin/
$ git svn fetch --log-window-size 10000 #CAUTION THIS LINE TAKES A LONG TIME TO COMPLETE
$ git reset --hard origin/trunk</pre>
4. Merge changes from Subversion to GitHub
<pre>$ git checkout svnsync
$ git svn rebase 
$ git checkout master 
$ git merge svnsync 
$ git push origin master</pre>
5. Merge changes from GitHub and publish to SubVersion
<pre>$ git checkout master
$ git pull origin master 
$ git checkout svnsync 
$ git svn rebase 
$ git merge --no-ff master 
$ git commit 
$ git svn dcommit</pre>
### Tagging Releases
Tagging a release in Git is very simple:

<code>$ git tag v1.0.4</code>

To create an SVN tag, simply:

<code>$ git svn tag 1.0.4</code>

This will create `/tags/1.0.4` in the remote SVN repository and copy all the files from the remote `/trunk` into that tag, so be sure to push all the latest code to `/trunk` before creating an SVN tag.

### Subversion tagging

It appears that there is now an issue with git svn tagging. We now have to tag using subversion directly.
Download code from svn Repo

<code>$ svn checkout https://plugins.svn.wordpress.org/stop-web-crawlers/
$ svn cp https://plugins.svn.wordpress.org/stop-web-crawlers/trunk https://plugins.svn.wordpress.org/stop-web-crawlers/tags/1.3.1</code>