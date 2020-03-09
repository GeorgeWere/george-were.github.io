---
layout: menu
title: "pppD Vulnerability"
description: "A critical Buffer Overflow vulnerability discovered in the pppD could let remote attackers exploit the Linux systems to gain the root-level privileges."
tags: [Linux, RCE, pppD]
date: "Posted on `r format(Sys.time(), '%d %B, %Y')`"
---

# <span style="color:red">Point-to-Point Protocol(PPP) Daemon RCE Vulnerability</span>
  posted on: 3/6/2020 5:14pm

---

## CVE-2020-8597: PPP Daemon RCE Vulnerability.

![PPP Daemon](./screenshots/pppd/icon.png)


- A critical __Buffer Overflow Vulnerability__ was discovered in the [pppD](https://linux.die.net/man/8/pppd) by security researcher  Ilja Van Sprundel which can let remote attackers exploit the linux systems remotely and gain the root-level previleges.

- This vulnerability resides in the Extensible Authentication Protocol(EAP) packet. An unauthenticated remote attacker may be able to cause a [stack buffer overflow](https://blog.rapid7.com/2019/02/19/stack-based-buffer-overflow-attacks-what-you-need-to-know/) by exploiting this vulnerability allowing them to remotely take over the code execution of a process and perform arbitrary code execution on the target system.

- The post __Critical Vulnerability in ppp Daemon Let Hackers Remotely Exploit the Linux Systems & Gain Root Access__ appeared first on [GBHackers](https://gbhackers.com/) and its being tracked as __CVE-2020-8597__ with a __9.3__ CVE score. it affects PPP Daemon versions 2.4.2 through 2.4.8.

- It could be exploited by sending an unsolicited malformed EAP packet to a vulnerable ppp client or a server.

> “This vulnerability is due to an error in validating the size of the input before copying the supplied data into memory. As the validation of the data size is incorrect, arbitrary data can be copied into memory and cause memory corruption possibly leading to execution of unwanted code.” reads the security advisory published by the expert.

> “The vulnerability is in the logic of the eap parsing code, specifically in the eap_request() and eap_response() functions in eap.c that are called by a network input handler.”

- Ilja Van Sprundel pointed out that pppd runs with high privileges and works in conjuction with kernel drivers hence the reason an attacker can execute arbitrary code with high privileges.

- This Vulnerability affects most popular Linux distributions.

    ... [Red Hat Enterprise Linux](https://www.debian.org/security/2020/dsa-4632)

    ... [Debian](https://www.debian.org/security/2020/dsa-4632)

    ... [Ubuntu](https://people.canonical.com/~ubuntu-security/cve/2020/CVE-2020-8597.html)

    ... [Fedora](https://access.redhat.com/security/cve/cve-2020-8597)

    ... [NetBSD](https://cvsweb.netbsd.org/bsdweb.cgi/src/external/bsd/ppp/dist/pppd/eap.c?only_with_tag=MAIN)

    ... [SUSE Linux](https://www.suse.com/security/cve/CVE-2020-8597/)


## Solution

- Update your software with the latest available patches provided by your software vendor.

> “It is incorrect to assume that pppd is not vulnerable if EAP is not enabled or EAP has not been negotiated by a remote peer using a secret or passphrase. This is due to the fact that an authenticated attacker may still be able to send unsolicited EAP packet to trigger the buffer overflow.” continues the advisory.

## References

```console
https://git.savannah.nongnu.org/cgit/lwip.git/commit/?id=2ee3cbe69c6d2805e64e7cac2a1c1706e49ffd86

https://nvd.nist.gov/vuln/detail/CVE-2020-8597

https://vulners.com/cve/CVE-2020-8597

https://github.com/paulusmack/ppp/commit/8d45443bb5c9372b4c6a362ba2f443d41c5636af

https://www.itsecuritynews.info/critical-vulnerability-in-ppp-daemon-let-hackers-remotely-exploit-the-linux-systems-gain-root-access/
```
