---
layout: org_default
title: Programs
subtitle: The work we run, and the editions we have held so far.
---

{% assign org = site.data.org %}

<div class="org-prose" markdown="1">

Everything we do is built around one goal: making it possible for researchers in and from developing
countries to do computer vision research, publish it, and be part of the international community that
reviews and builds on it.

</div>

## Our programs

<div class="row org-card-grid">
{% for program in org.programs %}
  <div class="col-md-4">
    <div class="org-card">
      <h3>{{ program.name }}</h3>
      <p class="org-card-meta"><em>{{ program.period }}</em></p>
      <p>{{ program.text }}</p>
      <p style="margin-top: 0.9rem"><a href="{{ program.link }}">{{ program.link-text }} &rarr;</a></p>
    </div>
  </div>
{% endfor %}
</div>

## Workshop editions

{% for edition in org.editions %}
<div class="org-edition">
  <div class="org-edition-year">{{ edition.year }}</div>
  <div class="org-edition-body">
    <h3>{{ edition.title }}{% if edition.status == 'upcoming' %}<span class="org-tag">Upcoming</span>{% endif %}</h3>
    <p>{{ edition.venue }} &middot; {{ edition.location }} &middot; {{ edition.date }}</p>
    <a href="{{ edition.url }}">Workshop site &rarr;</a>
  </div>
</div>
{% endfor %}

<div class="org-prose" markdown="1">

## Research topics we highlight

Past editions have featured disease detection in low-quality medical scans, road-safety assessment
from low-cost cameras, crop disease and agricultural monitoring, livestock health monitoring, school
mapping for connectivity, remote sensing, and OCR for underrepresented scripts — alongside method
work on efficient architectures, data-efficient and self-supervised learning, robustness to domain
shift, and multilingual vision–language models.

</div>

<div class="org-cta" markdown="0">
  <h2>Want to take part?</h2>
  <p>
    Calls for papers, challenge details and important dates for the current edition are published on
    the workshop site.
  </p>
  <a class="org-btn org-btn-solid" href="{{site.url}}/{{ site.data.cv4dc.current-year }}/">Go to the CV4DC {{ site.data.cv4dc.current-year }} workshop</a>
</div>
