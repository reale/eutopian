---
layout: page
title: Contattaci
lang: it
ref: contact-us
permalink: /it/partecipa/contattaci
child_of_ref: get-involved
order: 2
---

Contattaci utilizzando il form seguente:

<form name="contact-form" accept-charset="utf-8" action="https://formspree.io/f/mpzojrnr" method="post">
  <div class="field">
    <label for="full-name">Nome</label>
    <input type="text" name="name" id="full-name" />
  </div>
  <div class="field">
    <label for="email-address">Email</label>
    <input type="email" name="_replyto" id="email-address" required="" />
  </div>
  <div class="field">
    <label for="message">Messaggio</label>
    <textarea name="message" id="message" rows="4" required=""></textarea>
  </div>
  <div class="form-group">
    <input type="hidden" name="_language" value="{{ page.lang }}" />
    <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission">
  </div>

  <input type="submit" value="Invia" class="btn btn-primary btn-lg btn-block"/>
</form>
