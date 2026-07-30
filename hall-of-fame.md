---
layout: page
title: "Hall of Fame"
subtitle: "Vendor recognitions for reported security issues."
permalink: /hall-of-fame/
description: "Bug bounty hall-of-fame recognitions earned by Ali Sherif across Google, Apple, AWS, Cloudflare, IBM, BlackBerry and Mapbox."
---

Seven vendor programs have put my name on a page after I told them something they
would rather not have heard. Every report below went through coordinated disclosure,
which mostly means waiting patiently while a fix works its way through someone else's
release process.

<div class="card-list" style="margin-top:1.5rem;">
{%- for h in site.data.hof -%}
  {%- if h.url and h.url != "" -%}
  <a class="card" href="{{ h.url }}" rel="noopener" target="_blank">
  {%- else -%}
  <div class="card">
  {%- endif -%}
    <div class="card-meta">
      {%- if h.count and h.count != "" -%}<span class="badge status">{{ h.count }}</span>{%- endif -%}
      {%- if h.year and h.year != "" -%}<span>{{ h.year }}</span>{%- endif -%}
    </div>
    <h2 class="card-title">{{ h.org }}</h2>
    <p class="card-desc">{{ h.note }}</p>
    {%- if h.with and h.with != "" -%}<p class="card-sub">joint report with {{ h.with }}</p>{%- endif -%}
  {%- if h.url and h.url != "" -%}</a>{%- else -%}</div>{%- endif -%}
{%- endfor -%}
</div>

The Cloudflare report was joint work with my friend and fellow researcher
[Momen Ashraf](https://www.linkedin.com/in/momenashrafff/).

## Upstream fix

One finding did better than an acknowledgement and turned into a security patch
merged directly into a Google open source project, FlatBuffers (Swift runtime). A
detailed writeup is coming once the paperwork around it is done.
