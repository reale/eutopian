---
layout: page
title: Quota di iscrizione
description:
lang: it
ref: quota-iscrizione
permalink: /it/quota-iscrizione
---

La quota di iscrizione è fissata in 20 euro per il 2020. È possibile corrisponderla attraverso una delle due modalità seguenti:

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
      <script src="https://www.paypal.com/sdk/js?client-id=sb&currency=EUR" data-sdk-integration-source="button-factory"></script>
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
    </div>
  </div>
</div>

