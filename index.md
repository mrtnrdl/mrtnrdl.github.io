---
title: mrtns blog
---
<head>
<link rel="shortcut icon" type="image/png" href="assets/favicon-32x32.png">
<link rel="apple-touch-icon" sizes="180x180" href="assets/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="assets/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="assets/favicon-16x16.png">
<link rel="manifest" href="assets/site.webmanifest">
<link rel="mask-icon" href="assets/safari-pinned-tab.svg" color="#5bbad5">
<meta name="msapplication-TileColor" content="#da532c">
<meta name="theme-color" content="#ffffff">
</head>

### /me

coming from a background in development and consulting, the world if information security caught my attention several years ago. more recently i've started focussing on doing ctfs as well as learning about the tools, techniques and procedures that are used during red team engagements. 

besides infosec shenanigans, i spend my time playing guitar and the occasional game of dota or cs:go. 

if you want to follow me on social media, there is only <a rel="me" href="https://infosec.exchange/@0xmrtn">mastodon</a>.
### /blog


<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

you can also subscribe via [rss](https://blog.mrtnrdl.de/feed).
