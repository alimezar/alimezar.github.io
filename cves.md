---
layout: page
title: "CVEs"
subtitle: "Public disclosures. Documented impact. Fixes that ship."
permalink: /cves/
description: "16 CVE-assigned vulnerabilities by Ali Sherif. Explore public vulnerability details, severity sources, affected versions, and advisories."
wide: true
---
<div class="page-intro">
  <p><strong>{{ site.stats.cves }} CVE-assigned vulnerabilities</strong> across application frameworks, cloud tooling, security platforms, and the Go ecosystem. The public entries below link to vendor advisories or issue trackers.</p>
  <p class="muted small">{{ site.data.cves.size }} public entries listed. Severity and version information follow the linked sources. Assignment totals and the public list are tracked separately.</p>
</div>

<div class="cve-list">
{% for c in site.data.cves %}
<details class="cve-item" id="{{ c.id | downcase }}">
  <summary>
    <span class="cve-summary">
      <span class="card-meta"><span class="cve-id">{{ c.id }}</span><span>{{ c.vendor }}</span></span>
      <span class="cve-title">{{ c.title }}</span>
      <span class="cve-product">{{ c.product }}</span>
    </span>
    <span class="cve-right"><span class="badge {% if c.severity != '' %}sev-{{ c.severity | downcase }}{% else %}unrated{% endif %}">{% if c.severity != '' %}{{ c.severity }}{% else %}Unrated{% endif %}</span><span class="expand-icon" aria-hidden="true">+</span></span>
  </summary>
  <div class="cve-detail">
    {% if c.summary %}<p>{{ c.summary }}</p>{% endif %}
    <dl class="report-facts">
      {% if c.affected %}<div><dt>Affected</dt><dd>{{ c.affected }}</dd></div>{% endif %}
      {% if c.fixed_in %}<div><dt>Fixed in</dt><dd>{{ c.fixed_in }}</dd></div>{% endif %}
      {% if c.status %}<div><dt>Status</dt><dd>{{ c.status }}</dd></div>{% endif %}
      {% if c.score %}<div><dt>Severity source</dt><dd>CVSS {{ c.cvss_version }}: {{ c.score }} / {{ c.score_source }}</dd></div>{% endif %}
      {% if c.published %}<div><dt>Published</dt><dd>{{ c.published }}</dd></div>{% endif %}
    </dl>
    <div class="detail-links"><a class="text-link" href="{{ c.url }}" target="_blank" rel="noopener">Read source <span aria-hidden="true">↗</span><span class="sr-only"> (opens in a new tab)</span></a>{% if c.record_url %}<a class="text-link" href="{{ c.record_url }}" target="_blank" rel="noopener">CVE record ↗<span class="sr-only"> (opens in a new tab)</span></a>{% endif %}{% if c.writeup and c.writeup != '' %}<a class="text-link" href="{{ c.writeup | relative_url }}">Writeup →</a>{% endif %}</div>
  </div>
</details>
{% endfor %}
</div>

