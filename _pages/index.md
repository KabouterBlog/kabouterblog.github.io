---
layout: page
title: Home
id: home
permalink: /
---
# Welcome! 🌱

This garden contains the musings and ramblings
<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">

If you are unsure where to start, have a look at [[Bilbo, not Rambo]], which details the reason as to why I am doing this.

</p>
#### Recently updated notes
<ul>

{% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
{% for note in recent_notes limit: 5 %}
<li>
{{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
</li>
{% endfor %}
</ul>
