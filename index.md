---
layout: org_default
title: Home
hero: true
hero-title: Computer Vision for Developing Countries
hero-text: A non-profit organization that fosters and supports research in all aspects of computer vision for developing countries.
hero-cta: What we do
hero-cta-url: /programs
hero-cta2: Support our work
hero-cta2-url: /support
---

{% assign org = site.data.org %}

<div class="org-prose" markdown="1">

## Why this work matters

Much of the world's population lives in settings where vision systems have to work under real
constraints: limited compute, intermittent connectivity, low-cost or low-resolution sensors, scarce
labeled data, and many underserved languages. Research that takes these constraints seriously pushes
the whole field forward — but the researchers closest to those problems are often the furthest from
the venues where the field's work is reviewed, published and discussed.

Computer Vision for Developing Countries exists to close that gap. We build venues, mentorship and
funding paths so that researchers in and from developing countries can do their work, publish it, and
be part of the international computer vision community.

</div>

## What we do

<div class="row org-card-grid">
{% for pillar in org.pillars %}
  <div class="col-md-6 col-lg-3">
    <div class="org-card">
      <div class="org-card-icon"><i class="{{ pillar.icon }}"></i></div>
      <h3>{{ pillar.title }}</h3>
      <p>{{ pillar.text }}</p>
    </div>
  </div>
{% endfor %}
</div>

## Our workshop series

Our flagship program is the annual CV4DC Workshop, held with a major international computer vision
conference. Each edition brings together invited talks, oral and poster presentations, a panel
discussion and a dedicated mentoring session for junior researchers.

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

<div class="org-cta" markdown="0">
  <h2>Help us reach the next researcher</h2>
  <p>
    Sponsorship, mentoring and volunteer reviewing all go directly into keeping our programs open and
    free to attend for researchers from developing countries.
  </p>
  <a class="org-btn org-btn-solid" href="{{site.url}}/support">Ways to support us</a>
  <a class="org-btn" href="mailto:{{ org.email }}">Get in touch</a>
</div>
