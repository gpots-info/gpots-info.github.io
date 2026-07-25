---
layout: default
permalink: /
---

{%- assign next = site.data.meetings | where: "upcoming", true | first -%}
{%- assign prev = site.data.meetings | where_exp: "m", "m.upcoming != true" | first -%}

{%- if next %}
<div class="next-meeting">
  <p class="kicker">Next meeting</p>
  <h1 class="where">{{ next.host }}</h1>
  {%- if next.dates %}
  <p class="when">{{ next.dates }}</p>
  {%- endif %}
  {%- if next.organizers %}
  <p class="muted">Organized by {{ next.organizers | join: ", " }}.</p>
  {%- endif %}
  {%- if next.url %}
  <p><a href="{{ next.url }}">Conference website</a></p>
  {%- else %}
  <p class="muted">A conference website is not up yet. Announcements will go
  out on the <a href="/mailing-list/">mailing list</a>.</p>
  {%- endif %}
</div>
{%- else %}
<div class="next-meeting">
  <p class="kicker">Next meeting</p>
  <h1 class="where">Not yet announced</h1>
  <p class="muted">The next host has not been settled. Announcements go out on
  the <a href="/mailing-list/">mailing list</a>.</p>
</div>
{%- endif %}

{%- if prev %}
<div class="past-meeting">
  <p class="kicker">Most recent meeting</p>
  <p class="where">{{ prev.host }}</p>
  <p class="when">
    {{ prev.dates }}{% if prev.dates and prev.url %} · {% endif %}
    {%- if prev.url %}<a href="{{ prev.url }}">Conference website</a>{% endif %}
  </p>
</div>
{%- endif %}

GPOTS is an annual meeting in operator algebras and operator theory. It has been held every year since 1981 and has had continuous support from the National Science Foundation since 1983. A different university hosts each year.

Registration, the program, invited speakers, and local information all live on the host institution's own website for that year. This site exists to make the current meeting easy to find, to keep a record of [past meetings](/meetings/), and to help run the announcement list.

## Announcements

Announcements about future meetings go out on the [mailing list](/mailing-list/). It is low volume, a few messages a year, and you can leave at any time.

## Contact

For anything about the conference itself, write to [organizers@gpots.org](mailto:organizers@gpots.org). That address reaches whoever is organizing the next meeting.
