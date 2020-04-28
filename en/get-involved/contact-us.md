---
layout: page
title: Contact Us
lang: en
ref: contact-us
permalink: /en/get-involved/contact-us
child_of_ref: get-involved
order: 3
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
