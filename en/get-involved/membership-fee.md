---
layout: page
title: Membership Fee
description:
lang: en
ref: membership-fee
permalink: /en/get-involved/membership-fee
child_of_ref: get-involved
order: 3
---

The membership fee is as follows:

<table class="table">
  <tbody>
    <tr>
      <td>Individuals</td>
      <td>€50</td>
    </tr>
    <tr>
      <td>Students</td>
      <td>€20</td>
    </tr>
    <tr>
      <td>Startups, SMEs and business networks</td>
      <td>€150</td>
    </tr>
    <tr>
      <td>Non-profits</td>
      <td>€50</td>
    </tr>
    <tr>
      <td>Public bodies</td>
      <td>€50</td>
    </tr>
    <tr>
      <td>Large enterprises</td>
      <td>€500</td>
    </tr>
  </tbody>
</table>

You can pay it through one of the two following ways:

<div class="container">
  <div class="row">
    <div class="col-sm">
      <h2 id="wire-transfer">Wire transfer</h2>
      
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
