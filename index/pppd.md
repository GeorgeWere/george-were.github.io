---
layout: menu
title: "pppD Vulnerability"
description: "A critical Buffer Overflow vulnerability discovered in the pppD could let remote attackers exploit the Linux systems to gain the root-level privileges."
tags: [Linux, RCE, pppD]
---

# <span style="color:red">Point-to-Point Protocol(PPP) Daemon RCE Vulnerability</span>

---

## CVE-2020-8597: PPP Daemon RCE Vulnerability.

- A critical __Buffer Overflow Vulnerability__ was discovered in the [pppD](https://linux.die.net/man/8/pppd) by security researcher  Ilja Van Sprundel which can let remote attackers exploit the linux systems remotely and gain the root-level previleges.

- This vulnerability resides in the Extensible Authentication Protocol(EAP) packet. An unauthenticated remote attacker may be able to cause a [stack buffer overflow](https://blog.rapid7.com/2019/02/19/stack-based-buffer-overflow-attacks-what-you-need-to-know/) by exploiting this vulnerability allowing them to remotely take over the code execution of a process and perform arbitrary code execution on the target system.

- The post __Critical Vulnerability in ppp Daemon Let Hackers Remotely Exploit the Linux Systems & Gain Root Access__ appeared first on [GBHackers](https://gbhackers.com/) and its being tracked as __CVE-2020-8597__ with a __9.3__ CVE score. it affects PPP Daemon versions 2.4.2 through 2.4.8.

- It could be exploited by sending an unsolicited malformed EAP packet to a vulnerable ppp client or a server.

> “This vulnerability is due to an error in validating the size of the input before copying the supplied data into memory. As the validation of the data size is incorrect, arbitrary data can be copied into memory and cause memory corruption possibly leading to execution of unwanted code.” reads the security advisory published by the expert.

> “The vulnerability is in the logic of the eap parsing code, specifically in the eap_request() and eap_response() functions in eap.c that are called by a network input handler.”

- Ilja Van Sprundel pointed out that pppd runs with high privileges and works in conjuction with kernel drivers hence the reason an attacker can execute arbitrary code with high privileges.

- This Vulnerability affects most popular Linux distributions

## Solution

- Update your software with the latest available patches provided by your software vendor

> “It is incorrect to assume that pppd is not vulnerable if EAP is not enabled or EAP has not been negotiated by a remote peer using a secret or passphrase. This is due to the fact that an authenticated attacker may still be able to send unsolicited EAP packet to trigger the buffer overflow.” continues the advisory.
