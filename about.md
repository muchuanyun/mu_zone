---
layout: page
title: About
---

{% comment %}
  This inserts the "about" photo and text from `_config.yml`.
  You can edit it there (jekyll needs restart!) or remove it and provide your own photo/text.
  Don't forget to add the `me` class to the photo, like this: `![alt](src){:.me}`.
{% endcomment %}

{% if site.author.photo %}
  ![{{ site.author.name }}]({{ site.author.photo }}){:.me}
{% endif %}

{{ site.author.about }}

During the first twenty years of my life, I struggled to be know-it-all. For my remaining years, I accept my imperfect brain and just want to be a person who contributes something to the world.

##### This site is Built with [Jekyll](http://jekyllrb.com) and [Hydejack Theme](https://github.com/qwtel/hydejack.git).
