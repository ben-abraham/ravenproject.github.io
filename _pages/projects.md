---
layout: page-w-banner
title: Projects
bannerTitle: Ravencoin Projects
bannerImage: /assets/img/pages/exchanges/exchange-banner.jpg
permalink: /projects/
---

<div class="wrapper mt-16 pb-20">
  <h2>Current Ravencoin Projects</h2>
    <p></p>
      {% assign sorted_projects = site.data.projects | sort: "name" %}
      {% for project in sorted_projects %}
          <h3>{{ project.name }}</h3>          
          <p>{{ project.description }}</p>
          <h4>Project Websites</h4>
          <ul>
          {% for site in project.project_sites %}
          <li><a href="{{ site.url }}">{{ site.name }}</a></li>
          {% endfor %}
          </ul>
          <h4>Project Roadmap</h4>
          <ul>
          {% for value in project.roadmap %}
          <li>{{ value.name }} -- {{ value.value }}</li>
          {% endfor %}
          </ul>
          <h4>Get In Contact</h4>
          <ul>
          {% for site in project.social %}
          <li><a href="{{ site.url }}">{{ site.name }}</a></li>
          {% endfor %}
          </ul>
      {% endfor %}

</div>
