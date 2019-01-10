---
title: mrtns blog
---

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
