---
layout: default
permalink: /
---

{%- assign next = site.data.meetings | first -%}

<div class="next-meeting">
  <p class="kicker">Next meeting</p>
  <h1 class="where">{{ next.host }}</h1>
  <p class="when">{{ next.dates }}</p>
  {%- if next.organizers %}
  <p class="muted">Organized by {{ next.organizers | join: ", " }}.</p>
  {%- endif %}
  {%- if next.url %}
  <p><a href="{{ next.url }}">Conference website</a></p>
  {%- endif %}
</div>

GPOTS is the annual United States meeting in operator algebras and operator
theory. It has been held every year since 1981 and has had continuous support
from the National Science Foundation since 1983. A different university hosts
each year.

Registration, the program, invited speakers, and local information all live on
the host institution's own website for that year, linked above. This site
exists to make the current meeting easy to find, to keep a record of past ones,
and to run the announcement list.

## Keeping in touch

Announcements about future meetings go out on the [mailing
list](/mailing-list/). It is low volume, a few messages a year, and you can
leave at any time.

For anything about the conference itself, write to
[organizers@gpots.org](mailto:organizers@gpots.org). That address reaches
whoever is organizing the next meeting.
