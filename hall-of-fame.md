---
layout: page
title: "Recognition"
subtitle: "Acknowledgements from the teams behind the software."
permalink: /hall-of-fame/
description: "Security research recognition from Google, Apple, AWS, Cloudflare, IBM, BlackBerry, and Mapbox."
wide: true
---
<div class="page-intro"><p>Recognition from seven vendor programs for reported security issues and contributions. Public acknowledgement pages and advisory links are included where available.</p></div>
<div class="recognition-grid">
{% for h in site.data.hof %}
<article class="recognition-card">
  <div class="card-meta">{% if h.year and h.year != "" %}<span>{{ h.year }}</span>{% endif %}{% if h.count and h.count != "" %}<span>{{ h.count }}</span>{% endif %}</div>
  <h2>{{ h.org }}</h2><p>{{ h.note }}</p>
  {% if h.with and h.with != "" %}<p class="small muted">Joint report with {{ h.with }}.</p>{% endif %}
  {% if h.url and h.url != "" %}<a class="text-link" href="{{ h.url }}" target="_blank" rel="noopener">View source ↗<span class="sr-only"> (opens in a new tab)</span></a>{% endif %}
</article>
{% endfor %}
</div>
<p class="small muted">The Cloudflare report was joint work with <a href="https://www.linkedin.com/in/momenashrafff/">Momen Ashraf</a>.</p>
<section class="upstream-note"><p class="eyebrow">Beyond the report</p><h2>A fix contributed upstream.</h2><p>My FlatBuffers contribution fixes truncated scalar-vector verification in the Swift runtime and adds a regression test.</p><a class="text-link" href="https://github.com/google/flatbuffers/pull/9081" target="_blank" rel="noopener">View the merged pull request ↗<span class="sr-only"> (opens in a new tab)</span></a></section>

