---
layout: page
title: "About"
subtitle: "Who I am and what I work on."
permalink: /about/
description: "Ali Sherif, Security Engineer at IBM and vulnerability researcher."
---

I am **Ali Sherif**, a Security Engineer at **IBM** and an independent vulnerability
researcher. I look for the places where software trusts input it has no business
trusting, then write the finding up so the root cause is clear, not just the diff that
fixed it.

I do not have one favorite bug class. My reports range from a blind SSRF in an OAuth
avatar fetch to a stack overflow caused by a signed char, and the only thing they
really have in common is someone deciding a value was safe before checking.

## What I work on

- **Web and application security**: SSRF, path traversal, authentication and
  authorization logic, and the assumptions that hold up fine until someone sends two
  requests at the same time.
- **Cloud and infrastructure**: distributed agents, cluster protocols, and the CLI
  tooling that quietly writes your credentials to disk.
- **Parsers, deserialization, and memory safety**: binary formats, verifiers, and the
  gap between what a check promises and what the generated code actually does.
- **Bug bounty and coordinated disclosure**: reporting through vendor programs and
  staying with it until a fix actually ships.
- **CTF and HackTheBox**: keeping the offensive side sharp on a regular basis.

## Track record

- **10 assigned CVEs** across Google, AWS, IBM, Mapbox, Wazuh, Werkzeug and Gitea,
  including an XSS in Go's `html/template` and a critical path traversal to code
  execution in Wazuh's cluster sync.
- **Hall of Fame recognition** from Google, Apple, AWS, Cloudflare, IBM, BlackBerry
  and Mapbox.
- A **merged security fix in Google FlatBuffers** (Swift runtime). The writeup is
  written, it is just not public yet.
- **First place at ICMTC CTF 2026** and **second place at ICMTC CTF 2025**.
- Active on **HackTheBox**, solving machines on an ongoing basis.

See the [CVEs](/cves/) and [Hall of Fame](/hall-of-fame/) pages for the breakdown,
and [research](/research/) for technical writeups (coming soon).

## Contact

The best way to reach me about a security issue, a finding, or collaboration:

- GitHub: [@alimezar](https://github.com/alimezar)
- Email: [ali.mezar@gmail.com](mailto:ali.mezar@gmail.com)
