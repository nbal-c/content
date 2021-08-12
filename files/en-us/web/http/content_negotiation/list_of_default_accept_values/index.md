---
title: List of default Accept values
slug: Web/HTTP/Content_negotiation/List_of_default_Accept_values
tags:
  - Accept
  - Content Negotiation
  - HTTP
  - Reference
---
<div>{{HTTPSidebar}}</div>

<p>This article documents the default values for the HTTP <code><a href="/en-US/docs/Web/HTTP/Headers/Accept">Accept</a></code> header for specific inputs and browser versions.</p>

<h2 id="Default_values">Default values</h2>

<p>These are the values sent when the context doesn't give better information. Note that all browsers add the <code>*/*</code> MIME Type to cover all cases. This is typically used for requests initiated via the address bar of a browser, or via an HTML {{HTMLElement("a")}} element.</p>

<table>
  <tr>
    <th>User Agent</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>Firefox 72 and later [1]</td>
    <td><code>text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8</code></td>
  </tr>
  <tr>
    <td>Firefox 66 to 71 [1]</td>
    <td><code>text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8</code></td>
  </tr>
  <tr>
    <td>Firefox 65 [1]</td>
    <td><code>text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8</code></td>
  </tr>
  <tr>
    <td>Firefox 64 and earlier [1]</td>
    <td><code>text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8</code></td>
  </tr>
  <tr>
    <td>Safari, Chrome</td>
    <td><code>text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8</code></td>
  </tr>
  <tr>
    <td>Safari 5 [2]</td>
    <td><code>text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8</code></td>
  </tr>
  <tr>
    <td>Internet Explorer 8 [3]</td>
    <td><code>image/jpeg, application/x-ms-application, image/gif, application/xaml+xml, image/pjpeg, application/x-ms-xbap, application/x-shockwave-flash, application/msword, */*</code></td>
  </tr>
  <tr>
    <td>Edge</td>
    <td><code>text/html, application/xhtml+xml, image/jxr, */*</code></td>
  </tr>
  <tr>
    <td>Opera</td>
    <td><code>text/html, application/xml;q=0.9, application/xhtml+xml, image/png, image/webp, image/jpeg, image/gif, image/x-xbitmap, */*;q=0.1</code></td>
  </tr>
</table>

<p>[1] This value can be modified using the <a href="http://kb.mozillazine.org/Network.http.accept.default"><code>network.http.accept.default</code></a> parameter.</p>
<p>[2] This is an improvement over earlier <code>Accept</code> headers as it no longer ranks <code>image/png</code> above <code>text/html</code>.</p>
<p>[3] See <a href="https://docs.microsoft.com/en-us/archive/blogs/ieinternals/ie-and-the-accept-header">IE and the Accept Header (IEInternals' MSDN blog)</a>.</p>

<h2 id="Values_for_an_image">Values for an image</h2>

<p>When requesting an image, like through an HTML {{HTMLElement("img")}} element, user-agent often sets a specific list of media types to be welcomed.</p>

<table>
 <tbody>
  <tr>
   <th>User Agent</th>
   <th>Value</th>
  </tr>
  <tr>
   <td>Firefox 65 and later [1]</td>
   <td><code>image/webp,*/*</code></td>
  <tr>
    <td>Firefox 47 to 63 [1]</td>
    <td><code>*/*</code></td>
  </tr>
  <tr>
    <td>Firefox prior to 47 [1]</td>
    <td><code>image/png,image/*;q=0.8,*/*;q=0.5</code></td>
  </tr>
  <tr>
   <td>Safari (since Mac OS Big Sur)</td>
   <td><code>image/webp,image/png,image/svg+xml,image/*;q=0.8,video/*;q=0.8,*/*;q=0.5</code></td>
  </tr>
  <tr>
    <td>Safari (before Mac OS Big Sur)</td>
    <td><code>image/png,image/svg+xml,image/*;q=0.8,video/*;q=0.8,*/*;q=0.5</code></td>
  </tr>
  <tr>
   <td>Chrome</td>
   <td><code>image/avif,image/webp,image/apng,image/*,*/*;q=0.8</code></td>
  </tr>
  <tr>
    <td>Internet Explorer 9</td>
    <td><code>image/png,image/svg+xml,image/*;q=0.8, */*;q=0.5</code></td>
   </tr>
  <tr>
   <td>Internet Explorer 8 or earlier <em><a href="https://docs.microsoft.com/en-us/archive/blogs/ieinternals/ie-and-the-accept-header">source</a></em></td>
   <td><code>*/*</code></td>
  </tr>

 </tbody>
</table>

<p>[1] This value can be modified using the <code>image.http.accept</code> parameter (<em><a href="https://searchfox.org/mozilla-central/search?q=image.http.accept">source</a></em>).</p>

<h2 id="Values_for_a_video">Values for a video</h2>

<p>When a video is requested, via the {{HTMLElement("video")}} HTML element, most browsers use specific values.</p>

<table>
 <tbody>
  <tr>
   <th>User Agent</th>
   <th>Value</th>
  </tr>
  <tr>
    <td>Firefox 3.6 and later</td>
    <td><code>video/webm,video/ogg,video/*;q=0.9,application/ogg;q=0.7,audio/*;q=0.6,*/*;q=0.5</code></td>
  </tr>
  <tr>
   <td>Firefox earlier than 3.6</td>
   <td><em>no support for {{HTMLElement("video")}}</em></td>
  </tr>
  <tr>
   <td>Chrome</td>
   <td><code>*/*</code></td>
  </tr>
  <tr>
   <td>Internet Explorer 8 or earlier</td>
   <td><em>no support for {{HTMLElement("video")}}</em></td>
  </tr>
 </tbody>
</table>

<h2 id="Values_for_audio_resources">Values for audio resources</h2>

<p>When an audio file is requested, like via the {{HTMLElement("audio")}} HTML element, most browsers use specific values.</p>

<table class="standard-table">
 <tbody>
  <tr>
   <th>User Agent</th>
   <th>Value</th>
  </tr>
  <tr>
   <td>Firefox 3.6 and later [1]</td>
   <td><code>audio/webm,audio/ogg,audio/wav,audio/*;q=0.9,application/ogg;q=0.7,video/*;q=0.6,*/*;q=0.5</code></td>
  </tr>
  <tr>
   <td>Safari, Chrome</td>
   <td><code>*/*</code></td>
  </tr>
  <tr>
   <td>Internet Explorer 8 or earlier</td>
   <td><em>no support for {{HTMLElement("audio")}}</em></td>
  </tr>
  <tr>
   <td>Internet Explorer 9</td>
   <td>?</td>
  </tr>
 </tbody>
</table>

<p>[1] See <a href="https://bugzilla.mozilla.org/show_bug.cgi?id=489071">bug 489071</a>.</p>

<h2 id="Values_for_scripts">Values for scripts</h2>

<p>When a script is requested, like via the {{HTMLElement("script")}} HTML element, some browsers use specific values.</p>

<table>
 <tbody>
  <tr>
   <th>User Agent</th>
   <th>Value</th>
  </tr>
  <tr>
   <td>Firefox [1]</td>
   <td><code>*/*</code></td>
  </tr>
  <tr>
   <td>Safari, Chrome</td>
   <td><code>*/*</code></td>
  </tr>
  <tr>
   <td>Internet Explorer 8 or earlier [2]</td>
   <td><code>*/*</code></td>
  </tr>
  <tr>
   <td>Internet Explorer 9</td>
   <td><code>application/javascript, */*;q=0.8</code></td>
  </tr>
 </tbody>
</table>
<p>[1] See <a href="https://bugzilla.mozilla.org/show_bug.cgi?id=170789">bug 170789</a>.</p>
<p>[2] See <a href="https://docs.microsoft.com/en-us/archive/blogs/ieinternals/ie-and-the-accept-header">IE and the Accept Header (IEInternals' MSDN blog)</a>.</p>
<h2 id="Values_for_a_CSS_stylesheet">Values for a CSS stylesheet</h2>

<p>When a CSS stylesheet is requested, via the <code>&lt;link rel="stylesheet"&gt;</code> HTML element, most browsers use specific values.</p>

<table>
 <tbody>
  <tr>
   <th>User Agent</th>
   <th>Value</th>
  </tr>
  <tr>
   <td>Firefox 4 [1]</td>
   <td><code>text/css,*/*;q=0.1</code></td>
  </tr>
  <tr>
   <td>Internet Explorer 8 or earlier [2]</td>
   <td><code>*/*</code></td>
  </tr>
  <tr>
   <td>Internet Explorer 9</td>
   <td><code>text/css</code></td>
  </tr>
  <tr>
   <td>Safari, Chrome</td>
   <td><code>text/css,*/*;q=0.1</code></td>
  </tr>
  <tr>
   <td>Opera 11.10</td>
   <td><code>text/html, application/xml;q=0.9, application/xhtml+xml, image/png, image/webp, image/jpeg, image/gif, image/x-xbitmap, */*;q=0.1 </code></td>
  </tr>
  <tr>
   <td>Konqueror 4.6</td>
   <td><code>text/css,*/*;q=0.1</code></td>
  </tr>
 </tbody>
</table>
<p>[1] See <a class="link-https" href="https://bugzilla.mozilla.org/show_bug.cgi?id=170789">bug 170789</a>.</p>
<p>[2] See <a href="https://docs.microsoft.com/en-us/archive/blogs/ieinternals/ie-and-the-accept-header">IE and the Accept Header (IEInternals' MSDN blog)</a>.</p>