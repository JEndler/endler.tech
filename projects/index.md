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

# Startups

Currently I'm working on two startups, [Datapods](https://datapods.app) and [Robowriter](https://robowriter.de).

<ul class="list">

<li class="list__item">
  <span class="list__secondary-content">
    At Robowriter, we're trying to make Text-Generation AI as accessible as possible. We do this by abstracting away the process of model selection aswell as prompt engineering, and instead focus on providing a simple, easy to use template-interface for our users. We're live at [robowriter.de](https://robowriter.de) and have over 80 templates to try out.
  </span>
    Tech Stack: React, Tailwind, Firebase, Posthog(which is great), and a bunch of different LLMs.
</li>

<li class="list__item">
  <span class="list__secondary-content">
    At Datapods, we're building an app that allows individuals to request their personal data from big tech companies. Later, we'll also allow them to sell their data to companies, and get paid for it. We're planning on launching in Q3 2024. If you want to get in early, there's a waitlist on [datapods.app](https://datapods.app).
  </span>
    Tech Stack: Flutter, Supabase, Solidity, Lit-Protocol, Deno.
</li>

</ul>

# Close-source Projects

While I'm not at liberty to share the most of the projects I've done or work on in the scope of my previous jobs, I'm happy to describe some of them and describe them in more details privately via me via [jakob@endler.tech](mailto:jakob@endler.tech).

<ul class="list">

<li class="list__item">
  <span class="list__secondary-content">
    At DHL Data & Analytics i was working on a Project on Google Cloud Kubernetes Engine to setup automated Data Pipelining from an External Source, through Redpanda to ClickHouse for Analysis.
  </span>
    The whole deployment was setup via Terraform IaC and Kubernetes.

    - Technologies used: Google Cloud Platform, Python, ClickHouse, Kafka, Kubernetes, Terraform
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
    <a href="https://drive.google.com/file/d/10fqMpZL6u5bgeLMV97SkvcApwzSrqvwS/view?usp=sharing" target="_blank">Bachelor's Thesis: Simulating 5G Networks</a>
  </p>
  <span class="list__secondary-content">
    I wrote my bachelor's thesis in cooperation with the network planning team at Deutsche Telekom AG.
    My goal was to build a simulation for a specific 5G feature (MU-MIMO), to gather insight into how it would impact user performance.

    - Technologies used: MATLAB, Statistical Modeling, SQL
  </span>
</li>

</ul>

# Open-source Projects

<p>In my spare time i sometimes build some stuff, here's some of that :)</p>

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
