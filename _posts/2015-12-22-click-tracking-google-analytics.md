---
ID: 535
post_title: 'Click Tracking [Google Analytics]'
author: praison
post_excerpt: ""
layout: post
permalink: >
  https://praison.com/2015/12/click-tracking-google-analytics/
published: true
post_date: 2015-12-22 17:22:45
---
<h2>Event Tracking</h2>
<pre>&lt;script&gt;
/**
* Function that tracks a click on a link in Google Analytics.
* This function takes a valid URL string as an argument, and uses that URL string
* as the event label. Setting the transport method to 'beacon' lets the hit be sent
* using 'navigator.sendBeacon' in browser that support it.
*/
var trackLink = function(url) {
   ga('send', 'event', '<strong>link</strong>', '<strong>click</strong>', <strong>url</strong>, {
     'transport': 'beacon',
     'hitCallback': function(){document.location = url;}
   });
}
&lt;/script&gt;</pre>
<h2>On Page Implementation</h2>
<pre>&lt;a href="http://www.example.com" onclick="trackLink('http://www.example.com'); return false;"&gt;Visit example.com&lt;/a&gt;</pre>
&nbsp;