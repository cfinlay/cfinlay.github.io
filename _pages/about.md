---
permalink: /
title: "About"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I'm a post-doctoral researcher at [McGill University](https://www.mcgill.ca/) in machine learning. My PhD was in applied math, where I was supervised by 
[Adam Oberman](https://www.adamoberman.net/).  My research interests lie at the intersection of deep learning, machine learning, and applied math.

My current research includes robust optimization for deep neural networks,
unsupervised learning (density estimation and generative models), and neural
ODEs. I am also actively studying connections between Variational Calculus,
neural ODEs and optimal control.

Before jumping on the machine learning bandwagon, I studied numerical methods for solving nonlinear
elliptic Partial Differential Equations (PDEs). These are equations that
describe "diffusion-like" behaviour, in that they have properties very similar
to the Laplace operator. These types of equations are very common and describe
a wide range of physical phenomenon in physics and engineering, including optimal control (through the HJB operator) and inverse problems. 

Prior to grad school, I worked as a data analyst for [Natural Resources
Canada](https://www.nrcan.gc.ca/home).

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
