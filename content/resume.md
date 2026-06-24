+++
title = "Resume"
template = "page.html"
path = "resume"
+++

<div class="resume">

# Jason Fried

**Software Engineer** | Catheys Valley, California

📧 me@jasonfried.info | 🌐 jasonfried.info | 💻 github.com/fried | 🔗 linkedin.com/in/jasonandrewfried

---

## About

Software engineer with over 25 years in technology — from running a dial-up ISP as a high school sysadmin to spending the last 14 years as Meta's Python authority. At Meta, I've driven every major CPython upgrade from 2.7 through 3.14, led the company-wide Python 2→3 migration, and built the frameworks and tooling that keep Python performant at planet scale. Deep expertise in CPython internals, cross-language integration (C++/Rust), asyncio, and high-performance service architecture.

---

## Experience

### Meta (Facebook)

**2011–Present · 14 years**

#### Software Engineer — Dev Infrastructure: Python Language

*Sep 2015 – Present · Menlo Park, CA (Remote after 2022)*

Founded the Python Infrastructure team in 2015.

- **Work at a low level changing code that affects every Python service at Meta** — runtime, build system, RPC framework, cross-language integration layer. A single change lands across thousands of services. Own the rollouts end-to-end: compatibility testing, performance regression analysis, staged fleet-wide deployment, and incident response
- **Led every major CPython upgrade from 2.7 through 3.14** — debugging performance regressions introduced by runtime changes, managing cross-team compatibility, and coordinating fleet-wide rollout across thousands of services. Built the profiling and regression detection automation that made zero-downtime language version migrations possible at planet scale
- **Architected the asyncio-first rewrite of Meta's Python Thrift RPC framework** — improving service concurrency and tail latency across the entire Python service stack. Authored `ServiceDecorator`, the decorator-based framework that became the standard way to launch a production Python Thrift RPC service at Meta
- **Pioneered Cython adoption at Meta**, introducing and evangelizing Cython as a performance bridge between Python and native code, enabling critical hot paths to achieve near-C performance without sacrificing developer velocity
- **Recognized as the go-to expert for complex CPython debugging**, specializing in cross-language integration at the CPython/C++/Rust boundary — diagnosing memory corruption, GIL contention, segfaults in native extensions, and ABI compatibility problems that few engineers in the industry can resolve
- **Recognized as Meta's asyncio expert**, the authority on async Python patterns, performance, and debugging. Debugged a SEV where nested event loops were spawning thousands of event loops — latency tanked to minutes. Patched the library to reuse event loops from a stack: 2 event loops, sub-second latency. A true single-event-loop fix was ~2% faster but required major service changes — stack reuse shipped in time to resolve the SEV
- **Folly / cross-language Python integration** — pioneered the asyncio ↔ Folly coroutine bridge: Python code can await C++ coroutines and C++ can await Python coroutines. Created `folly/python/Weak.h` — reference Python from C/C++ without unconditionally linking CPython at runtime, allowing Python-specific behavior in widely-used C++ libraries with CPython linked only when the service actually uses Python. **Cut CPython linking in non-Python binaries from 76% to ~6% (C++/Rust/Go/OCaml/Haskell — tens of thousands of binaries).** Both open sourced in Folly
- Own build infrastructure and developer tooling on the Buck2/Starlark build system, directly impacting developer velocity across the engineering organization

#### Production Engineer

*Jan 2014 – Sep 2015 · Menlo Park, CA*

- **Led Meta's Python 2 → 3 migration**, the multi-year effort to modernize one of the world's largest Python codebases across thousands of services and millions of lines of code
- **Designed and built FBPKG**, the blob shipping service for all containers at Meta — Instagram, facebook.com, and internal systems. End-to-end design: client, server, and data API. HA orchestration handling regular ad-hoc swarms across 100s of thousands of machines, with constant package ingestion available globally at a moment's notice. DR for FBPKG's own self-hosting binaries. **Massively scalable**: when a Chef misconfig triggered a datacenter-wide thundering herd — every machine pulling gigabytes every 15 minutes — FBPKG didn't blink. Planned for 5 years before major scaling improvements were needed — made it 7. Service is still in use as of 2026
- **Delivered 255x faster machine name provisioning** — unique machine naming required updates across several systems, a slow process done 1 machine at a time. Worked with each system maintainer to discover the maximum safe batch size, turning 1-at-a-time naming into 255 machines at a time at the same latency

#### Operations Engineer

*Oct 2011 – Jan 2014 · Menlo Park, CA*

- Site reliability and infrastructure operations for facebook.com during a period of rapid growth — from 800M to over one billion monthly active users
- **Helped services migrate from bare metal into Tupperware** (Meta's pre-Kubernetes container orchestration platform) — wrote automation to convert deployment configuration into scheduler/container configurations, moving large production services off bare metal into the container platform
- On-call for one of the highest-traffic web properties on the planet, responsible for incident response and operational tooling
- Built automated host health detection and remediation tooling across the fleet

---

### Deloitte Consulting

**May 2009 – Oct 2011 · 2 yrs 6 mos**

#### Consultant

*Dec 2009 – Oct 2011*

- Infrastructure deployments, version control systems, and issue tracking systems for enterprise clients
- Bridged the gap between operations and development teams on large-scale consulting engagements

#### Senior Analyst

*May 2009 – Dec 2009*

- Internal cloud support and system administration
- Built a self-service portal for account creation and password recovery for internal Windows domain, reducing help desk ticket volume

---

### BearingPoint Inc.

#### Senior Technology Analyst

*Jun 2006 – May 2009 · 3 yrs*

- Introduced to virtualization with VMware vSphere, driving a consolidation that grew the managed environment from 7 physical machines to hundreds of VMs across a handful of physical hosts
- Developed internal self-service web applications for DNS management, IP reservations, disk space monitoring, and more
- Infrastructure and application development across diverse client engagements — server architecture, management tooling, and cross-domain technical support

---

### Southeastern Louisiana University — Administrative Computing Services

#### Network Technician

*2003–2006 · Hammond, LA*

- Installed and maintained equipment in the campus data center
- Automated routine administration tasks and scripted network statistics gathering/graphing
- Systems testing and validation for new infrastructure deployments

---

### East Baton Rouge Parish Schools

#### Systems Administrator

*1999–2000 · High School*

- Administered network infrastructure and systems for a student/teacher dial-up ISP operated by East Baton Rouge Parish Schools, located in the office of Scotlandville Magnet High School
- Managed user accounts, connectivity, and system reliability — first sysadmin role at age 17

---

## Open Source

- **`later`** — Asyncio service toolbox (PyPI); the foundation for how asyncio code is tested inside Meta
- **CPython** — contributor to the reference Python implementation, with landed pull requests in the core project
- **Folly (`folly/python`)** — contributor across Meta's open-source C++ `folly/python` layer — authored `folly/python/Weak.h`, pioneered the asyncio ↔ Folly coroutine bridge

---

## Talks

- **Upgrading Python at Extreme Scales** — PyCon US 2025 · https://www.youtube.com/watch?v=2b-SeACd3tM
- **The Future is Async** — PyCon US 2022 · https://www.youtube.com/watch?v=XW7yv6HuWTE — asyncio anti-patterns and bad behavior
- **Changing the Culture Around Python 2 → 3 Migration at Facebook** — PyCon US 2017 · https://www.youtube.com/watch?v=H4SS9yVWJYA

---

## Education

### Southeastern Louisiana University

**BS, Computer Science** · 2000–2006

- Summer 2005 President's List
- Chapter President, ACM Student Chapter (Senior Year)
- Systems Administrator, ACM Unix server (2002–2006)
- ACM International Collegiate Programming Contest (ICPC) — Regionals 2001–2004, highest-ranking SLU team each year
- Organized SLUgo, a 24-hour gaming convention on campus (2005, 2006)

</div>
