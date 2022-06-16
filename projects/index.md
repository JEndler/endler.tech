---
layout: default
title: "Projects"
excerpt: "A list of all my open-sourced projects, all hosted on GitHub. Fair warning: some of them are not maintained anymore."
tags:
  - projects
  - open-source
  - closed-source
  - github
---

# Close-source Projects

While I'm not at liberty to share the most of the projects I've done or work on in the scope of my previous jobs, I'm happy to describe some of them and describe them in more details privately via me via [jakob@endler.tech](mailto:jakob@endler.tech).

<ul class="list">
<li class="list__item">
  <p class="list__primary-content">
    <a href="https://drive.google.com/file/d/1dwwnV0e5TIMnji26SzE1Dm-8-61juipS/view?usp=sharing" target="_blank">Project Paper (in German)</a>
  </p>
  <span class="list__secondary-content">
    During my time at Deutsche Telekom AGs Network Service and Automation divison i was tasked with the experimental development of a anomaly detection system for our OpenStack environments.
    Unfortunately this project is still used internally and thus a am not allowed to publish the code.
  </span>
</li>


# Open-source Projects

Early in my carreer I used to invest a lot more time in open-source projects. Here are a few of them I initiated myself or contributed to.

{% assign groups = site.data.projects|group_by:"category" %}
{% assign groups = groups|sort:"name" %}
{% for category in groups %}

  <h2>{{ category.name }}</h2>
  <ul class="list">
  {% assign projects = category.items|sort:"name" %}
  {% for project in projects %}
    <li class="list__item">
      <p class="list__primary-content">
        <a href="{{ project.link }}" target="_blank">{{ project.name }}</a>
      </p>
      <span class="list__secondary-content">{{ project.description }}</span>
    </li>
  {% endfor %}
{% endfor %}
