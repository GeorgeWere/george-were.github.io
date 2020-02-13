---
title: "HTB WRITE-UPS"
layout: menu
description: "Retired HackTheBox Machine Write-ups"
header-img: "chals/htb/htb.png"
tags: [HackTheBox, htb, boot2root, solutions, solution, writeup, write-up, machines, machine, linux, windows, openbsd, stratosphere, poison, canape, sunday, devoops, tartarsauce, jerry, hawk, active, waldo, mischief, teacher, irked, lightweight, chaos, help, flujab, friendzone, ctf, luke, kryptos, swagshop, writeup, ellingson, safe, pentest, pentesting, penetration testing]
boxes: [
    [AI, "", "./boxes/14_AI.html", orange, Linux, 10.10.10.163, 30 pts,  "Dec 16, 2018"],
]
---

## <span style="color:red">$ htb write-ups</span>

---

<div style="overflow-x:auto">
  <table>
    <tr>
      <td><strong style="text-decoration:underline">BOX NAME</strong></td>
      <td><strong style="text-decoration:underline">OS</strong></td>
      <td><strong style="text-decoration:underline">MACHINE IP</strong></td>
      <td><strong style="text-decoration:underline">RETIRED</strong></td>
    </tr>
    {% for box in page.boxes %}{% if box[2] != "" %}
    <tr>
      <td><a href="{{ box[2] }}">{{ box[0] }}</a> {% if box[1] != "" %}({{box[1]}}){% endif %}</td>
      <td><span style="color:{{ box[3] }}">{{ box[4] }}</span></td>
      <td><span style="color:{{ box[3] }}">{{ box[5] }}</span></td>
      <td>{{ box[7] }}</td>
    </tr>
    {% endif %}{% endfor %}
    {% for box in page.boxes %}{% if box[2] == "" %}
    <tr>
      <td>{{ box[0] }} {% if box[1] != "" %}({{box[1]}}){% endif %}</td>
      <td><span style="color:{{ box[3] }}">{{ box[4] }}</span></td>
      <td><span style="color:{{ box[3] }}">{{ box[5] }}</span></td>
      <td>{{ box[7] }}</td>
    </tr>
    {% endif %}{% endfor %}
  </table>
</div>

---

### LEGEND : <strong style="color:green">EASY (20 pts)</strong> | <strong style="color:orange">MEDIUM (30 pts)</strong> | <strong style="color:red">HARD (40 pts)</strong> | <strong style="color:white">INSANE (50 pts)</strong>
