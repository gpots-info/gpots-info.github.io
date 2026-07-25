---
layout: default
title: Past meetings
permalink: /meetings/
---

GPOTS has met annually since 1981, first as the Great Plains Operator Theory
Seminar and under its present name since 1989. Where a year's website still
exists, the year is a link to it.

Some entries are incomplete. If you can fill in a gap or correct an error,
write to [webmaster@gpots.org](mailto:webmaster@gpots.org).

<div class="table-wrap">
<table>
  <thead>
    <tr>
      <th>Year</th>
      <th>Host</th>
      <th>Dates</th>
      <th>Organizers</th>
    </tr>
  </thead>
  <tbody>
  {%- for m in site.data.meetings %}
    <tr>
      <td class="year">
        {%- if m.url %}<a href="{{ m.url }}">{{ m.year }}</a>{% else %}{{ m.year }}{% endif -%}
      </td>
      <td>
        {%- if m.host %}{{ m.host }}{% else %}<span class="unknown">unknown</span>{% endif -%}
        {%- if m.note %}<span class="note">{{ m.note }}</span>{% endif -%}
      </td>
      <td>{{ m.dates }}</td>
      <td>{% if m.organizers %}{{ m.organizers | join: ", " }}{% endif %}</td>
    </tr>
  {%- endfor %}
  </tbody>
</table>
</div>
