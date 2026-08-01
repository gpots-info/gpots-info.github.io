---
layout: default
title: Mailing list
permalink: /mailing-list/
---

The GPOTS mailing list carries announcements about upcoming meetings.

Your address is not shared with anyone other than the organizers.

## Subscribe

{% comment %}
The form posts to the list server, which sends the confirmation and then
redirects to /mailing-list/check-your-email/. The "trap" field is a bot
trap: it is positioned off screen by the stylesheet, so anything typed
into it means the submission was not made by a person.
{% endcomment %}

<form class="subscribe" action="https://lists.gpots.org/subscribe" method="post">
  <div class="field">
    <label for="sub-email">Email address</label>
    <input type="email" id="sub-email" name="email" required autocomplete="email">
  </div>
  <div class="field">
    <label for="sub-name">Name (optional)</label>
    <input type="text" id="sub-name" name="display_name" autocomplete="name">
  </div>
  <div class="trap" aria-hidden="true">
    <label for="sub-website">Leave this field empty</label>
    <input type="text" id="sub-website" name="website" tabindex="-1" autocomplete="off">
  </div>
  <button type="submit">Subscribe</button>
</form>

You will be sent a message asking you to confirm. Nothing is added to the list until you answer it.

## Leaving the list

Send an empty message to [announce-leave@gpots.org](mailto:announce-leave@gpots.org) and you are removed straight away. That address is also at the bottom of every message the list sends.

If an address on the list is wrong or out of date, write to [webmaster@gpots.org](mailto:webmaster@gpots.org).
