---
title: mrtns blog
---

### /me

i'm a 30 year old infosec person. coming from a background in development and consulting, the world if information security caught my attention several years ago. more recently i've started focussing on doing ctfs as well as learning about the tools, techniques and procedures that are used during red team engagements. 

### /blog


<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
