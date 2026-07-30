---
layout: page
title: "CVEs"
subtitle: "Confirmed vulnerabilities with assigned identifiers."
permalink: /cves/
description: "Confirmed CVEs assigned to Ali Sherif, across Google, AWS, IBM, Mapbox, Wazuh, Werkzeug and Gitea."
wide: true
---

Ten identifiers so far, spread across cloud tooling, security platforms, developer
SDKs, and open source web infrastructure. All ten are public. A few point at the
vendor advisory or the issue tracker instead of cve.org, because the CVE record is
still working its way through the system.

Severity is whatever the published record says, not my own opinion of how interesting
the bug was. The two rarely agree. The Go entry sits up top without a rating, because
the fix has not shipped and nobody has scored it yet.

<div class="table-scroll">
<table class="cve-table">
  <thead>
    <tr><th>ID</th><th>Vulnerability</th><th>Vendor</th><th>Severity</th><th>Year</th></tr>
  </thead>
  <tbody>
    {%- for c in site.data.cves -%}
    <tr{% if c.pending %} class="pending"{% endif %}>
      <td class="cve-id">{%- if c.url and c.url != "" -%}<a href="{{ c.url }}" rel="noopener" target="_blank">{{ c.id }}</a>{%- else -%}{{ c.id }}{%- endif -%}</td>
      <td>{{ c.title }}{%- if c.writeup and c.writeup != "" -%} &middot; <a href="{{ c.writeup | relative_url }}">writeup</a>{%- endif -%}</td>
      <td class="cve-vendor">{{ c.vendor }}</td>
      <td>{%- if c.severity and c.severity != "" -%}<span class="badge sev-{{ c.severity | downcase }}">{{ c.severity }}</span>{%- else -%}<span class="badge">unrated</span>{%- endif -%}</td>
      <td class="cve-year">{{ c.year }}</td>
    </tr>
    {%- endfor -%}
  </tbody>
</table>
</div>

<p class="muted" style="font-family:var(--font-mono);font-size:.82rem;">
Updated as records publish and embargoes lift. Reserved entries appear here without
details until the advisory is out.
</p>
