---
layout: org_default
title: About us
subtitle: Who we are, what we stand for, and how we are registered.
---

{% assign org = site.data.org %}

<div class="org-prose" markdown="1">

## Our mission

</div>

<div class="org-mission">
  <p>{{ org.mission }}</p>
</div>

<div class="org-prose" markdown="1">

## Who we are

We are a group of computer vision researchers working in academia and industry across Asia, Europe
and North America, many of us from developing countries ourselves. We came together in 2024 around a
simple observation: excellent computer vision research is being done in developing regions, and the
international community sees far too little of it.

What began as a single workshop at ACCV 2024 in Hanoi has become an annual series, a community
challenge and a mentoring program. In {{ org.founded }} we formally established Computer Vision for
Developing Countries as a non-profit organization so that this work has a durable home — one that can
accept support, plan beyond a single conference cycle, and keep our programs free for the people they
are meant to serve.

## What we believe

**Constraints are a research direction, not a limitation.** Efficient architectures, data-efficient
and self-supervised learning, robustness to domain shift, and multilingual vision–language models are
advanced by taking real-world constraints seriously.

**Proximity matters.** The researchers closest to a problem — road safety, crop disease, medical
imaging on older equipment, scripts with little digital presence — bring context that cannot be
recovered from a dataset alone.

**Access is the bottleneck.** Talent is distributed evenly; travel funding, review networks,
mentorship and compute are not. Most of what we do is aimed squarely at that gap.

**Participation is open to everyone.** Our programs are open to all researchers. We give particular
emphasis to contributions from authors affiliated with developing countries.

## Leadership

</div>

{% if org.show-board %}
<div class="row org-person-grid">
{% for person in org.board %}
  <div class="col-6 col-md-3">
    <div class="org-person">
      {% if person.image %}
      <a href="{{ person.url }}" target="_blank"><img alt="{{ person.name }}" src="{{site.url}}/{{ person.image }}"></a>
      {% endif %}
      <p class="org-person-name"><a href="{{ person.url }}" target="_blank">{{ person.name }}</a></p>
      <p class="org-person-role">{{ person.role }}</p>
      <p class="org-person-affil">{{ person.affiliation }}</p>
    </div>
  </div>
{% endfor %}
</div>

{% if org.advisors %}
<h3 class="org-subhead">Advisory board</h3>
<div class="row org-person-grid">
{% for person in org.advisors %}
  <div class="col-6 col-md-3">
    <div class="org-person">
      {% if person.image %}
      <a href="{{ person.url }}" target="_blank"><img alt="{{ person.name }}" src="{{site.url}}/{{ person.image }}"></a>
      {% endif %}
      <p class="org-person-name"><a href="{{ person.url }}" target="_blank">{{ person.name }}</a></p>
      <p class="org-person-role">{{ person.role }}</p>
      <p class="org-person-affil">{{ person.affiliation }}</p>
    </div>
  </div>
{% endfor %}
</div>
{% endif %}
{% endif %}

<div class="org-prose" markdown="1">

## Organizing team

Beyond the officers, our programs are run by a volunteer committee of researchers. The current
organizing committee for the {{ org.editions[0].year }} edition is listed on the workshop site.

<p><a class="org-btn org-btn-solid" href="{{site.url}}/{{ org.editions[0].year }}/people">See the organizing committee</a></p>

## Organization details

</div>

<table class="org-facts">
  <tbody>
    <tr>
      <th scope="row">Legal name</th>
      <td>{{ org.name }}</td>
    </tr>
    <tr>
      <th scope="row">Type</th>
      <td>Non-profit organization{% if org.has-501c3 %}, 501(c)(3) tax-exempt{% endif %}</td>
    </tr>
    <tr>
      <th scope="row">Founded</th>
      <td>{{ org.founded }}</td>
    </tr>
    <tr>
      <th scope="row">Entity number</th>
      <td>{{ org.entity-number }}</td>
    </tr>
    <tr>
      <th scope="row">EIN</th>
      <td>{{ org.ein }}</td>
    </tr>
    <tr>
      <th scope="row">Contact</th>
      <td><a href="mailto:{{ org.email }}">{{ org.email }}</a></td>
    </tr>
  </tbody>
</table>

{% if org.has-501c3 %}
<div class="org-prose" markdown="1">

{{ org.tax-status }} {{ org.tax-deductible-note }}

</div>
{% endif %}
