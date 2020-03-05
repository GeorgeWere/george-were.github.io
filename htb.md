---
title: "HTB WRITE-UPS"
layout: menu
description: "Retired HackTheBox Machine Write-ups"
header-img: "chals/htb/htb.png"
tags: [AI,RE]
boxes: [
    [AI, "", "./boxes/14_AI.html", orange, Linux, 10.10.10.163, 30 pts,  "Jan 25, 2020"],
    [RE, "", "./boxes/2_RE.html", red, Windows, 10.10.10.144, 40 pts, "Feb 1, 2020"],
    [JSON, "", "./boxes/3_JSON.html", orange, Windows, 10.10.10.158, 30 pts, "Feb 15, 2020"],
    [Zetta, "", "./boxes/4_Zetta.html", red, Linux, 10.10.10.156, 40 pts, "Feb 22, 2020"],
]
---

## <span style="color:red">$ htb write-ups</span>

- Hack The Box is an online platform allowing you to test your penetration testing skills and exchange ideas and methodologies with other members of similar interests. It contains several challenges that are constantly updated. Some of them simulating real-world scenarios and some of them leaning more towards a CTF style of challenge.

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
