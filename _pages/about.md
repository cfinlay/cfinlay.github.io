---
permalink: /
title: "About"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I'm a research scientist at [Deep Render](https://deeprender.ai/), working in image and video compression.
Previously I was a post-doc at [McGill University](https://www.mcgill.ca/), in machine learning. My PhD was in applied math, where I was supervised by 
[Adam Oberman](https://www.adamoberman.net/).  My research interests lie at the intersection of deep learning, machine learning, and applied math.

<div>
  <h2>news</h2>
  {% if site.news  %}
    <table class="{{ include.type | default: "table" }}" style="margin-top: 1em; border: none; font-size: 14px;">
    {% assign news = site.news | reverse %}
    {% for item in news limit: site.news_limit %}
      <tr>
        <td style="border: none;" width="15%">{{ item.date | date: "%b %-d, %Y" }}</td>
        <td style="border: none;">
          {% if item.inline %}
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
          {% else %}
            <a href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a>
          {% endif %}
        </td>
      </tr>
    {% endfor %}
    </table>
  {% else %}
    <p>No news so far...</p>
  {% endif %}
</div>
