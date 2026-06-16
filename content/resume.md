+++
title = "Resume"
template = "page.html"
path = "resume"
+++

<div class="resume">

# Jason Fried

**Software Engineer** | Catheys Valley, California  
📧 me@jasonfried.info | 🌐 [jasonfried.info](https://jasonfried.info) | 🔗 [LinkedIn](https://www.linkedin.com/in/jasonandrewfried/)

---

## About

Software engineer with over 25 years in technology — from running a dial-up ISP as a high school sysadmin to spending the last 14 years as Meta's Python authority. At Meta, I've driven every major CPython upgrade from 2.7 through 3.14, led the company-wide Python 2→3 migration, and built the frameworks and tooling that keep Python performant at planet scale. Deep expertise in CPython internals, cross-language integration (C++/Rust), and high-performance service architecture.

---

## Experience

### Meta (Facebook)
**Full-time · Since 2011 · 14 years**

**Software Engineer — Dev Infrastructure: Python Language**  
*Sep 2015 – Present · Menlo Park, CA (Remote after 2022)*

- **Stewarded Python at Facebook/Meta**, owning language strategy, runtime upgrades, and tooling for one of the world's largest Python deployments
- **Led every major CPython upgrade from 2.7 through 3.14**, managing cross-team compatibility, performance regression testing, and fleet-wide rollout coordination across thousands of services
- **Pioneered Cython adoption at Facebook**, introducing and evangelizing Cython as a performance bridge between Python and native code, enabling critical hot paths to achieve near-C performance without sacrificing developer velocity
- **Architected a major modernization of the Python Thrift RPC framework**, redesigning the stack to be asyncio-first — improving concurrency, reducing latency, and aligning Meta's Python service infrastructure with modern async patterns
- **Authored `ServiceDecorator`, the decorator-based framework that became the most popular way to stand up a Python Thrift RPC server at Meta**, abstracting away service boilerplate so engineers could launch production services with minimal code
- **Recognized as the go-to expert for complex CPython debugging**, specializing in cross-language integration issues at the CPython/C++/Rust boundary — diagnosing memory corruption, GIL contention, segfaults in native extensions, and ABI compatibility problems that few engineers in the industry can resolve
- **Recognized as Meta's asyncio expert**, the authority on async Python patterns, performance, and debugging across the company's service infrastructure
- Own build infrastructure and developer tooling on the Buck2/Starlark build system, directly impacting developer velocity across the engineering organization

**Production Engineer**  
*Jan 2014 – Sep 2015 · Menlo Park, CA*

- **Primary driver of Meta's Python 2 to 3 migration**, leading the multi-year effort to modernize one of the world's largest Python codebases across thousands of services and millions of lines of code
- Designed and built FBPKG, the blob shipping service used to distribute binary artifacts across Meta's global infrastructure, serving Instagram, facebook.com, and internal systems
- Developed system provisioning automation for fleet-scale deployments

**Operations Engineer**  
*Oct 2011 – Jan 2014 · Menlo Park, CA*

- Site reliability and infrastructure operations for facebook.com during a period of rapid growth — from 800M to over one billion monthly active users
- On-call for one of the highest-traffic web properties on the planet, responsible for incident response and operational tooling
- Built various tools to automate the detection and remediation of host issues across the fleet

---

### Deloitte Consulting
**May 2009 – Oct 2011 · 2 yrs 6 mos**

**Consultant**  
*Dec 2009 – Oct 2011*

- Infrastructure deployments, version control systems, and issue tracking systems for enterprise clients
- Bridged the gap between operations and development teams on large-scale consulting engagements

**Senior Analyst**  
*May 2009 – Dec 2009*

- Internal cloud support and system administration
- Built a self-service portal for account creation and password recovery for internal Windows domain, reducing help desk ticket volume

---

### BearingPoint Inc.
**Senior Technology Analyst**  
*Jun 2006 – May 2009 · 3 yrs*

- Introduced to virtualization with VMware vSphere, driving a consolidation that grew the managed environment from 7 physical machines to hundreds of VMs across a handful of physical hosts
- Developed internal self-service web applications for DNS management, IP reservations, disk space monitoring, and more
- Infrastructure and application development across diverse client engagements — server architecture, management tooling, and cross-domain technical support

---

### East Baton Rouge Parish Schools
**Systems Administrator**  
*1999–2000 · High School*

- Administered network infrastructure and systems for a student/teacher dial-up ISP operated by East Baton Rouge Parish Schools, located in the office of Scotlandville Magnet High School
- Managed user accounts, connectivity, and system reliability — first sysadmin role at age 17

---

## Open Source

- **CPython** — contributor to the reference Python implementation, with landed pull requests in the core project
- **Folly (`folly/python`)** — contributor across much of Meta's open-source C++ `folly/python` layer; authored `folly/python/weak.h`, a mechanism for writing C++ that runs CPython-dependent logic only when CPython is actually linked into the running binary — avoiding the previous behavior of forcing CPython to be linked
- **`later`** — A toolbox for asyncio services (PyPI); the foundation for how asyncio code is tested inside Meta

---

## Education

### Southeastern Louisiana University
**BS, Computer Science** · 2000 – 2006

- Summer 2005 President's List
- Chapter President of ACM Student Chapter (Senior Year)
- Systems Administrator for ACM's local Unix server (2002–2006)
- Organized SLUgo, a 24-hour gaming convention on campus (2005, 2006)

</div>
