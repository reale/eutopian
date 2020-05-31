---
layout: page
title: Diventa Socio
lang: it
ref: membership
permalink: /it/partecipa/diventa-socio
child_of_ref: get-involved
order: 1
---

Per chiedere di diventare socio, compila il modulo seguente.

In alternativa, puoi scaricare e compilare il [Modulo di adesione per persone fisiche](/assets/docs/eutopian-adesione-persone-fisiche.docx) oppure il [Modulo di adesione per persone giuridiche](/assets/docs/eutopian-adesione-persone-giuridiche.docx) ed inviarlo a <a href="mailto:{{ site.email }}">{{ site.email }}</a>.

<form id="fs-frm" name="registration-form" accept-charset="utf-8" action="https://formspree.io/{{ site.email }}" method="post">
  <fieldset id="fs-frm-inputs">
    <div class="field">
      <label for="full-name">Nome e cognome</label>
      <input class="form-control" type="text" name="full-name" id="full-name" required>
    </div>

    <div class="field">
      <label for="full-name">Luogo di nascita</label>
      <input class="form-control" type="text" name="birth-place" id="birth-place" required>
    </div>

    <div class="field it-datepicker-wrapper">
      <label for="full-name">Data di nascita (gg/mm/anno)</label>
      <input class="form-control it-date-datepicker" id="birth-date" type="text" required placeholder="">
    </div>

    <div class="field">
      <label for="full-name">Professione</label>
      <input class="form-control" type="text" name="profession" id="profession" required>
    </div>

    <div class="field">
      <label for="full-name">Codice Fiscale</label>
      <input class="form-control" type="text" name="fiscal-code" id="fiscal-code" required>
    </div>

    <div class="field">
      <label for="full-name">Email</label>
      <input class="form-control" type="email" name="_replyto" id="email-address" required>
    </div>

    <div class="field">
      <label for="full-name">Telefono</label>
      <input class="form-control" type="text" name="phone-number" id="phone-number" required>
    </div>

    <div class="field">
      <label for="full-name">Comune o Stato estero di residenza</label>
      <input class="form-control" type="text" name="city" id="city" required>
    </div>

    <div class="field">
      <label for="full-name">Note aggiuntive</label>
      <textarea class="form-control" rows="2" name="note" id="note"></textarea>
    </div>

    <div class="form-group">
      <input type="hidden" name="_language" value="{{ page.lang }}" />
      <input type="hidden" name="_subject" id="email-subject" value="Richiesta di iscrizione">
    </div>

    <p>Io sottoscritta/o</p>

    <p class="text-center">MANIFESTO LA MIA VOLONTÀ</p>

    <p>di aderire all’Associazione “EUTOPIAN – OSSERVATORIO EUROPEO SULL’INNOVAZIONE DEMOCRATICA”, ai sensi e per gli effetti di cui all’art. 8.f del vigente <a href="/it/chi-siamo/statuto">Statuto</a> sociale</p>

    <p class="text-center">DICHIARO</p>

    <ul>
      <li>di condividere ed essere interessato alla realizzazione delle finalità della Associazione, di cui condivido lo spirito e gli ideali;</li>
      <li>di impegnarmi ad osservare lo Statuto, i Regolamenti interni e le deliberazioni legittimamente adottati dagli Organi associativi che dichiaro di aver letto attentamente e di accettare integralmente;</li>
      <li>di impegnarmi a corrispondere la quota di iscrizione, fissata nella misura di 20 EUR per il 2020.</li>
    </ul>

    <p>Autorizzo inoltre al trattamento di tutti i dati riportati nel presente modulo di adesione, compresi i futuri eventuali aggiornamenti e/o modifiche, per tutte le finalità statutarie dell’Associazione “EUTOPIAN – OSSERVATORIO EUROPEO SULL’INNOVAZIONE DEMOCRATICA” e nelle modalità descritte dalla <a href="/it/privacy-policy">Privacy Policy</a>.</p>

    <input type="submit" value="Invia" class="btn btn-primary btn-lg btn-block">
  </fieldset>
</form>
