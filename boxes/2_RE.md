---
layout: menu
title: "HTB Safe"
description: "10.10.10.144 | 40 pts"
header-img: "boxes/screenshots/2_RE/re.png"
tags: [hackthebox, htb, re, ai]
---
# HTB AI (10.10.10.144) MACHINE WRITE-UP

![80 AI Icon](./screenshots/14_ai/2_icon.png)
---

### TABLE OF CONTENTS
* [PART 1 : INITIAL RECON](#part-1--initial-recon)
* [PART 2 : PORT ENUMERATION](#part-2--port-enumeration)
  * [TCP PORT 80 (http)](#tcp-port-80-http)
* [PART 3 : EXPLOITATION](#part-3--exploitation)
* [PART 4 : GENERATE USER SHELL](#part-4--generate-user-shell)
* [PART 5 : LATERAL MOVEMENT (nobody -&gt; monitor)](#part-5--lateral-movement-nobody---monitor)
* [PART 6 : PRIVILEGE ESCALATION (monitor -&gt; root)](#part-6--privilege-escalation-monitor---root)

---

## PART 1 : INITIAL RECON
