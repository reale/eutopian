---
layout: page
title: Contatti
lang: it
ref: contacts
permalink: /it/contatti
order: 6
---

<p>Scrivici un messaggio o seguici sui nostri canali social.</p>

<form name="simple-contact-form" accept-charset="utf-8" action="https://formspree.io/{{ site.email }}" method="post">
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
  <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission">
  <ul class="actions">
    <li><input type="submit" value="Invia" /></li>
  </ul>
</form>
