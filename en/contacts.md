---
layout: page
title: Contacts
lang: en
ref: contacts
permalink: /en/contacts
order: 6
---

Contact us by filling the following form:

<form name="simple-contact-form" accept-charset="utf-8" action="https://formspree.io/{{ site.email }}" method="post">
  <div class="field">
    <label for="full-name">Name</label>
    <input type="text" name="name" id="full-name" />
  </div>
  <div class="field">
    <label for="email-address">Email Address</label>
    <input type="email" name="_replyto" id="email-address" required="" />
  </div>
  <div class="field">
    <label for="message">Message</label>
    <textarea name="message" id="message" rows="4" required=""></textarea>
  </div>
  <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission">
  <input type="submit" value="Invia" />
</form>
