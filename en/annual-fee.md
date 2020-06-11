---
layout: page
title: Annual Fee
description:
lang: en
ref: annual-fee
permalink: /en/annual-fee
---

The registration fee is set at 20 euros for 2020. It can be paid in one of the following two ways:

## Wire transfer

```
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
```

## PayPal

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
