---
layout: page
title: "CVEs"
subtitle: "Confirmed vulnerabilities with assigned identifiers."
permalink: /cves/
description: "Confirmed CVEs assigned to Ali Sherif."
---

Confirmed vulnerabilities with assigned CVE identifiers. Additional identifiers
have been assigned for findings that are not yet publicly disclosed, and will be
added here once embargoes lift.

<table>
  <thead>
    <tr><th>ID</th><th>Vulnerability</th><th>Vendor</th><th>Severity</th><th>Year</th><th>Status</th></tr>
  </thead>
  <tbody>
    {%- for c in site.data.cves -%}
    <tr>
      <td>{%- if c.url and c.url != "" -%}<a href="{{ c.url }}" rel="noopener" target="_blank">{{ c.id }}</a>{%- else -%}{{ c.id }}{%- endif -%}</td>
      <td>{{ c.title }}{%- if c.writeup and c.writeup != "" -%} &middot; <a href="{{ c.writeup | relative_url }}">writeup</a>{%- endif -%}</td>
      <td>{{ c.vendor }}</td>
      <td><span class="badge sev-{{ c.severity | downcase }}">{{ c.severity }}</span></td>
      <td>{{ c.year }}</td>
      <td>{{ c.status }}</td>
    </tr>
    {%- endfor -%}
  </tbody>
</table>

<p class="muted" style="font-family:var(--font-mono);font-size:.82rem;">
Counts and embargoed entries are kept current as disclosures are cleared.
</p>
