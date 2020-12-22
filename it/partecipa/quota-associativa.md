---
layout: page
title: Quota associativa
description:
lang: it
ref: membership-fee
permalink: /it/partecipa/quota-associativa
child_of_ref: get-involved
order: 3
---

La quota associativa è fissata come segue:

<table class="table">
  <tbody>
    <tr>
      <td>Persone fisiche</td>
      <td>€50</td>
    </tr>
    <tr>
      <td>Studenti</td>
      <td>€20</td>
    </tr>
    <tr>
      <td>Startup, PMI e reti d’impresa</td>
      <td>€150</td>
    </tr>
    <tr>
      <td>Associazioni</td>
      <td>€50</td>
    </tr>
    <tr>
      <td>Enti pubblici</td>
      <td>€50</td>
    </tr>
    <tr>
      <td>Grandi imprese</td>
      <td>€500</td>
    </tr>
  </tbody>
</table>

È possibile corrisponderla attraverso una delle due modalità seguenti:

<div class="container">
  <div class="row">
    <div class="col-sm">
      <h2 id="wire-transfer">Bonifico bancario</h2>
      
      <pre>
      ACCOUNT HOLDER
      Eutopian
      
      IBAN
      BE27 9671 1158 9873
      
      BANK CODE (SWIFT / BIC)
      TRWIBEB1XXX
      
      ADDRESS
      TransferWise Europe SA
      Avenue Marnix 13-17
      Brussels
      1000
      Belgium
      </pre>
    </div>
    <div class="col-sm">
      <h2 id="paypal-payment">PayPal</h2>
      
      <div id="paypal-button-container"></div>
    </div>
  </div>
</div>

<script src="https://www.paypal.com/sdk/js?client-id=AXPsjHSz9jJpvLxZcInFXlj1GFtu8bG52R2b4VEF7-DfExMXr7KK9ICq-I2NSerIRbFAJiwM7O-tLlGS&currency=EUR" data-sdk-integration-source="button-factory"></script>
<script>
  paypal.Buttons({
      style: {
          shape: 'rect',
          color: 'gold',
          layout: 'horizontal',
          label: 'paypal',

      },
      createOrder: function(data, actions) {
          return actions.order.create({
              purchase_units: [{
                  amount: {
                      value: '20'
                  }
              }]
          });
      },
      onApprove: function(data, actions) {
          return actions.order.capture().then(function(details) {
              alert('Transaction completed by ' + details.payer.name.given_name + '!');
          });
      }
  }).render('#paypal-button-container');
</script>
