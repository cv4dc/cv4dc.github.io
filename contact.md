---
layout: org_default
title: Contact
subtitle: How to reach the organization.
---

{% assign org = site.data.org %}

<div class="org-prose" markdown="1">

For anything concerning the organization — sponsorship, partnerships, volunteering, the workshop
series or the challenge — email us and the organizing committee will reply.

</div>

<div class="row org-card-grid">
  <div class="col-md-6">
    <div class="org-card">
      <div class="org-card-icon"><i class="far fa-envelope"></i></div>
      <h3>Email</h3>
      <p><a href="mailto:{{ org.email }}">{{ org.email }}</a></p>
    </div>
  </div>
  <div class="col-md-6">
    <div class="org-card">
      <div class="org-card-icon"><i class="fas fa-globe-asia"></i></div>
      <h3>Workshop series</h3>
      <p><a href="{{site.url}}/{{ site.data.cv4dc.current-year }}/">CV4DC {{ site.data.cv4dc.current-year }} workshop</a></p>
    </div>
  </div>
</div>

<div class="org-prose" markdown="1">

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
      <th scope="row">Entity number</th>
      <td>{{ org.entity-number }}</td>
    </tr>
    <tr>
      <th scope="row">EIN</th>
      <td>{{ org.ein }}</td>
    </tr>
  </tbody>
</table>
