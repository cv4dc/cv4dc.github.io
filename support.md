---
layout: org_default
title: Support us
subtitle: Sponsorship, volunteering and partnerships keep our programs open and free to attend.
---

{% assign org = site.data.org %}

<div class="org-prose" markdown="1">

We are a volunteer-run non-profit. Support goes directly into the things that decide whether a
researcher in a developing country can take part: registration and travel costs, workshop
organization, and the mentoring and review work around it.

{% if org.has-501c3 %}
{{ org.tax-status }} {{ org.tax-deductible-note }} Our EIN is **{{ org.ein }}**, which you can use for
employer matching-gift programs.
{% endif %}

</div>

## Ways to support

<div class="row org-card-grid">
{% if org.has-501c3 %}
  <div class="col-md-6 col-lg-3">
    <div class="org-card">
      <h3>Donate</h3>
      <p>Individual gifts of any size fund travel and registration support for presenting authors. As a 501(c)(3) organization, we can issue a receipt for your records.</p>
      <p style="margin-top: 0.9rem">
        {% if org.donate-url %}
        <a href="{{ org.donate-url }}">Make a donation &rarr;</a>
        {% else %}
        <a href="mailto:{{ org.email }}?subject=Donation%20to%20CV4DC">Email us for giving instructions &rarr;</a>
        {% endif %}
      </p>
    </div>
  </div>
{% endif %}
{% for item in org.support %}
  <div class="col-md-6 col-lg-3">
    <div class="org-card">
      <h3>{{ item.title }}</h3>
      <p>{{ item.text }}</p>
    </div>
  </div>
{% endfor %}
</div>

<div class="org-prose" markdown="1">

## Where support goes

- **Travel and registration support** for presenting authors from developing countries.
- **Keeping attendance free**, so cost is never the reason someone misses the workshop.
- **Running the challenge**, including data preparation and evaluation infrastructure.
- **The mentoring program**, matching junior researchers with senior members of the community.

## How to give

{% for method in org.giving %}
**{{ method.title }}.** {{ method.text }}
{% endfor %}

<p><a class="org-btn org-btn-solid" href="mailto:{{ org.email }}?subject=Donation%20to%20CV4DC">Email us to give</a></p>

## Tax-deductibility and receipts

{% if org.has-501c3 %}
{{ org.name }} is a 501(c)(3) tax-exempt organization, EIN {{ org.ein }}, registered under entity
number {{ org.entity-number }}. {{ org.tax-deductible-note }} No goods or services are provided in
exchange for a donation unless we state otherwise in writing. Email us and we will send a written
acknowledgment for your gift.
{% endif %}

## Talk to us about sponsorship

We work with each sponsor individually on the level of support and how your organization is
acknowledged across the workshop site and on-site materials. Write to us and we will send you the
current sponsorship information.

</div>

<div class="org-cta" markdown="0">
  <h2>Get in touch</h2>
  <p>Tell us how you would like to help and we will follow up with details.</p>
  <a class="org-btn org-btn-solid" href="mailto:{{ org.email }}">Email {{ org.email }}</a>
</div>
