---
layout: page
title: Become a Member
lang: en
ref: membership
permalink: /en/get-involved/become-member
child_of_ref: get-involved
order: 2
---

In order to become a member, please fill this form.

Alternatively, you may fill in either the [Application form for natural persons](/assets/docs/eutopian-adesione-persone-fisiche.docx) (in Italian only) or the [Application form for legal entities](/assets/docs/eutopian-adesione-persone-giuridiche.docx) (in Italian only), sign it (digitally or by attaching an ID document), and send it to <a href="mailto:{{ site.email }}">{{ site.email }}</a>.

<form id="fs-frm" name="registration-form" accept-charset="utf-8" action="https://formspree.io/f/xeqppkwv" method="post">
  <fieldset id="fs-frm-inputs">
    <div class="field">
      <label for="full-name">Full Name</label>
      <input class="form-control" type="text" name="full-name" id="full-name" required>
    </div>

    <div class="field">
      <label for="full-name">Birthplace</label>
      <input class="form-control" type="text" name="birth-place" id="birth-place" required>
    </div>

    <div class="field it-datepicker-wrapper">
      <label for="full-name">Birth Date (dd/mm/yyyy)</label>
      <input class="form-control it-date-datepicker" id="birth-date" type="text" required placeholder="">
    </div>

    <div class="field">
      <label for="full-name">Profession</label>
      <input class="form-control" type="text" name="profession" id="profession" required>
    </div>

    <div class="field">
      <label for="full-name">Fiscal Code, TIN, or equivalent</label>
      <input class="form-control" type="text" name="fiscal-code" id="fiscal-code" required>
    </div>

    <div class="field">
      <label for="full-name">Email Address</label>
      <input class="form-control" type="email" name="_replyto" id="email-address" required>
    </div>

    <div class="field">
      <label for="full-name">Phone Number</label>
      <input class="form-control" type="text" name="phone-number" id="phone-number" required>
    </div>

    <div class="field">
      <label for="full-name">City or foreign Country (if outside Italy) of residence</label>
      <input class="form-control" type="text" name="city" id="city" required>
    </div>

    <div class="field">
      <label for="full-name">Notes</label>
      <textarea class="form-control" rows="2" name="note" id="note"></textarea>
    </div>

    <div class="form-group">
      <input type="hidden" name="_language" value="{{ page.lang }}" />
      <input type="hidden" name="_subject" id="email-subject" value="Membership request">
    </div>

    <p>I the undersigned</p>

    <p class="text-center">EXPRESS MY WISH</p>

    <p>to join the “EUTOPIAN - EUROPEAN OBSERVATORY ON DEMOCRATIC INNOVATION”, pursuant to and for the purposes of art. 8.f of the current <a href="/en/about-us/statute">Statute</a>.</p>

    <p class="text-center">DECLARE</p>

    <ul>
      <li>to commit myself to the realisation of the aims of the Association, whose spirit and ideals I fully endorse;</li>
      <li>to commit myself to observing the Statute, the internal Regulations and deliberations adopted by the Association Bodies which I declare that I have read carefully and accept verbatim;</li>
      <li>to commit myself to pay the <a href="/en/get-involved/membership-fee">membership fee</a>.</li>
    </ul>

    <p>Furthermore, I authorise the processing of all the data contained herein, including any future updates and/or changes, for all statutory purposes of the Association “EUTOPIAN - EUROPEAN OBSERVATORY ON DEMOCRATIC INNOVATION”, as described in the <a href="/en/privacy-policy"> Privacy Policy </a>.</p>

    <input type="submit" value="Submit" class="btn btn-primary btn-lg btn-block">
  </fieldset>
</form>
