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
  <span class="list__secondary-content">
    I'm currently working on a Project on Google Cloud Kubernetes Engine to setup automated Data Pipelining from an External Source, through Redpanda to ClickHouse for Analysis.
    The whole deployment is setup via Terraform IaC and Kubernetes.I'm currently working on a Project on Google Cloud Kubernetes Engine to setup automated Data Pipelining from an External Source, through Redpanda to ClickHouse for Analysis. The whole deployment is setup via Terraform IaC and Kubernetes.

    - Technologies used: Google Cloud Platform, Python, ClickHouse, Kafka, Kubernetes, Terraform
  </span>
</li>

<li class="list__item">
  <p class="list__primary-content">
    <a href="https://drive.google.com/file/d/1dwwnV0e5TIMnji26SzE1Dm-8-61juipS/view?usp=sharing" target="_blank">Openstack Anomaly Root Cause Analysis</a>
  </p>
  <span class="list__secondary-content">
    During my time at Deutsche Telekom AGs Network Service and Automation divison i was tasked with the experimental development of a anomaly detection system for our OpenStack environments.
    Unfortunately this project is still used internally and thus a am not allowed to publish the code.

    - Technologies used: Elasticsearch, Logstash, Python, Docker
  </span>
</li>


<li class="list__item">
  <p class="list__primary-content">
    <a href="https://drive.google.com/file/d/1dwwnV0e5TIMnji26SzE1Dm-8-61juipS/view?usp=sharing" target="_blank">Bachelor's Thesis: Simulating 5G Networks</a>
  </p>
  <span class="list__secondary-content">
    I wrote my bachelor's thesis in cooperation with the network planning team at Deutsche Telekom AG.
    My goal was to build a simulation for a specific 5G feature (MU-MIMO), to gather insight into how it would impact user performance.

    - Technologies used: MATLAB, Statistical Modeling, SQL
  </span>
</li>


# Open-source Projects

In my spare time i sometimes build some stuff, here's some of that :)

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
