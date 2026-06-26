---
layout: page
title: "Hall of Fame"
subtitle: "Vendor recognitions for reported security issues."
permalink: /hall-of-fame/
description: "Bug bounty hall-of-fame recognitions earned by Ali Sherif across Google, Apple, Cloudflare, IBM, and BlackBerry."
---

Recognition from vendor security programs for responsibly disclosed issues, plus a
merged upstream fix. Each report was handled through coordinated disclosure.

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
  {%- if h.url and h.url != "" -%}</a>{%- else -%}</div>{%- endif -%}
{%- endfor -%}
</div>

## Upstream fix

Beyond program acknowledgements, one finding resulted in a security patch merged
directly into a Google open source project, FlatBuffers (Swift runtime). A detailed
technical writeup is coming soon.
