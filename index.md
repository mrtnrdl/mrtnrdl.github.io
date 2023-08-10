---
title: mrtns blog
---
<head>
	<link rel="shortcut icon" type="image/x-icon" href="favicon.ico">
	<link rel="apple-touch-icon" sizes="180x180" href="assets/apple-touch-icon.png">
	<link rel="icon" type="image/png" sizes="32x32" href="assets/favicon-32x32.png">
	<link rel="icon" type="image/png" sizes="16x16" href="assets/favicon-16x16.png">
	<link rel="manifest" href="assets/site.webmanifest">
	<link rel="mask-icon" href="assets/safari-pinned-tab.svg" color="#5bbad5">
	<meta name="msapplication-TileColor" content="#da532c">
	<meta name="theme-color" content="#ffffff">
</head>

## /me

Coming from a background in development and consulting, the world of information security caught my attention several years ago. From writing secure code I joined the dark(er) side and joined the attackers. Recently I'm doing CTFs as well as learning more about the tools, techniques and procedures that are used in pentests or from adversaries. 

Besides infosec shenanigans, i spend my time playing guitar and the occasional video gaming. 

If you want to follow me on social media, you can do this on <a rel="me" href="https://infosec.exchange/@0xmrtn">mastodon</a> and <a href="https://twitch.tv/0xmrtn">twitch</a>. 


If you want to hire me - have a look at my [CV](pages/cv) and take it from there. 

## /blog

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


## /subscribe
[click here](https://blog.mrtnrdl.de/feed) to get the rss feed.


## /pgp

pubkey fingerprint

`96EE 569A ADCE EC7A 756E E73F C797 7BAB 290A CBB8`

[public key](pages/pubkey.asc)

## /legal

[Imprint / Impressum](pages/imprint)
