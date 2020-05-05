---
layout: page
title: Become a Member
lang: en
ref: membership
permalink: /en/get-involved/become-member
child_of_ref: get-involved
order: 1
---

In order to become a member, please fill this form.

Alternatively, you may fill in either the [Application form for natural persons](/assets/docs/eutopian-adesione-persone-fisiche.docx) (in Italian only) or the [Application form for legal entities](/assets/docs/eutopian-adesione-persone-giuridiche.docx) (in Italian only), sign it (digitally or by attaching an ID document), and send it to <a href="mailto:{{ site.email }}">{{ site.email }}</a>.

<form id="fs-frm" name="registration-form" accept-charset="utf-8" action="https://formspree.io/{{ site.email }}" method="post">
  <fieldset id="fs-frm-inputs">
    <div class="form-group">
        <input class="form-control" type="text" name="full-name" id="full-name" placeholder="Full Name" required>
        <label for="full-name">I the undersigned</label>
    </div>
    <div class="form-group">
        <input class="form-control" type="text" name="birth-place" id="birth-placd" placeholder="Birthplace" required>
        <label for="full-name">Birthplace</label>
    </div>
    <div class="it-datepicker-wrapper">
        <div class="form-group">
            <input class="form-control it-date-datepicker" id="birth-date" type="text" placeholder="please insert the date in the format dd/mm/yyyy" required>
            <label for="birth-date">Birthdaty</label>
        </div>
    </div>
    <div class="form-group">
        <input class="form-control" type="text" name="profession" id="profession" placeholder="Profession" required>
        <label for="profession">Profession</label>
    </div>
    <div class="form-group">
        <input class="form-control" type="text" name="fiscal-code" id="fiscal-code" placeholder="Fiscal Code" required>
        <label for="fiscal-code">Fiscal Code or equivalent</label>
    </div>
    <div class="form-group">
        <input class="form-control" type="email" name="_replyto" id="email-address" placeholder="email@domain.tld" required>
        <label for="email-address">Email Address</label>
    </div>
    <div class="form-group">
        <input class="form-control" type="text" name="phone-number" id="phone-number" placeholder="Phone Number" required>
        <label for="phone-number">Phone Number</label>
    </div>
    <div class="form-group">
        <input class="form-control" type="text" name="city" id="city" placeholder="City" required>
        <label for="city">City</label>
    </div>
    <div class="form-group">
        <textarea class="form-control" rows="2" name="note" id="note" placeholder="Notes"></textarea>
        <label for="note">Notes</label>
    </div>
    <div class="form-group">
        <input type="hidden" name="_language" value="{{ page.lang }}" />
        <input type="hidden" name="_subject" id="email-subject" value="Registration Form Submission">
    </div>

    <p class = "text-center">EXPRESS MY WISH</p>

    <p class="text-justify">to join the “EUTOPIAN - EUROPEAN OBSERVATORY ON DEMOCRATIC INNOVATION”, pursuant to and for the purposes of art. 8.f of the current Statute.</p>

    <p class = "text-center"> DECLARE </p>

    <ul class = "text-justify">
      <li>to commit myself to the realisation of the aims of the Association, whose spirit and ideals I fully endorse;</li>
      <li>to commit myself to observing the Statute, the internal Regulations and deliberations adopted by the Association Bodies which I declare that I have read carefully and accept verbatim;</li>
      <li>to commit myself to pay the admission fee, if so established by the Board of Directors of the Association.</li>
    </ul>

    <p class="text-justify">The undersigned authorises the processing of all the data contained herein, including any future updates and/or changes, for all statutory purposes of the Association “EUTOPIAN - EUROPEAN OBSERVATORY ON DEMOCRATIC INNOVATION”, as described in the <a href="/en/privacy-policy"> Privacy Policy </a>.</p>

    <input type = "submit" value = "submit" class="btn btn-primary">
  </fieldset>
</form>
