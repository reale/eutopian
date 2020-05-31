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
    <input class="form-control" type="text" name="full-name" id="full-name" placeholder="Nome e cognome" required>
    <input class="form-control" type="text" name="birth-place" id="birth-place" placeholder="Luogo di nascita" required>
    <div class="it-datepicker-wrapper">
      <input class="form-control it-date-datepicker" id="birth-date" type="text" placeholder="Data di nascita (gg/mm/aaaa)" required>
    </div>
    <input class="form-control" type="text" name="profession" id="profession" placeholder="Professione" required>
    <input class="form-control" type="text" name="fiscal-code" id="fiscal-code" placeholder="Codice Fiscale" required>
    <input class="form-control" type="email" name="_replyto" id="email-address" placeholder="Email" required>
    <input class="form-control" type="text" name="phone-number" id="phone-number" placeholder="Telefono" required>
    <input class="form-control" type="text" name="city" id="city" placeholder="Comune di residenza" required>
    <textarea class="form-control" rows="2" name="note" id="note" placeholder="Informazioni aggiuntive"></textarea>

    <div class="form-group">
        <input type="hidden" name="_language" value="{{ page.lang }}" />
        <input type="hidden" name="_subject" id="email-subject" value="Richiesta di iscrizione">
    </div>

    <p class="text-center">MANIFESTO LA MIA VOLONTÀ</p>

    <p>di aderire all’Associazione “EUTOPIAN – OSSERVATORIO EUROPEO SULL’INNOVAZIONE DEMOCRATICA”, ai sensi e per gli effetti di cui all’art. 8.f del vigente <a href="/it/chi-siamo/statuto">Statuto</a> sociale</p>

    <p class="text-center">DICHIARO</p>

    <ul>
      <li>di condividere ed essere interessato alla realizzazione delle finalità della Associazione, di cui condivido lo spirito e gli ideali;</li>
      <li>di impegnarmi ad osservare lo Statuto, i Regolamenti interni e le deliberazioni legittimamente adottati dagli Organi associativi che dichiaro di aver letto attentamente e di accettare integralmente;</li>
      <li>di impegnarmi a corrispondere la quota di ammissione, ove stabilita dal Consiglio Direttivo dell’Associazione.</li>
    </ul>

    <p>La/Il Sottoscritta/o autorizza al trattamento di tutti i dati riportati nel presente modulo di adesione, compresi i futuri eventuali aggiornamenti e/o modifiche dallo/a stesso/a comunicate, per tutte le finalità statutarie dell’Associazione “EUTOPIAN – OSSERVATORIO EUROPEO SULL’INNOVAZIONE DEMOCRATICA” e nelle modalità descritte dalla <a href="/it/privacy-policy">Privacy Policy</a>.</p>

    <input type="submit" value="Invia" class="btn btn-primary btn-lg btn-block">
  </fieldset>
</form>
