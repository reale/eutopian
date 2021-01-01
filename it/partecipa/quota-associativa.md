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
      <div id="smart-button-container">
      <h2 id="paypal-payment">PayPal</h2>
            <div style="text-align: center;">
        <div style="margin-bottom: 1.25rem;">
          <p>Quota annuale</p>
          <select id="item-options"><option value="Persone fisiche	" price="50">Persone fisiche	 - 50 EUR</option><option value="Studenti" price="20">Studenti - 20 EUR</option><option value="Startup, PMI e reti d’impresa" price="150">Startup, PMI e reti d’impresa - 150 EUR</option><option value="Associazioni" price="50">Associazioni - 50 EUR</option><option value="Enti pubblici" price="50">Enti pubblici - 50 EUR</option><option value="Grandi imprese" price="500">Grandi imprese - 500 EUR</option></select>
                    <select style="visibility: hidden" id="quantitySelect"></select>
        </div>
      
      <div id="paypal-button-container"></div>
      </div>
    </div>
  </div>
</div>

<script src="https://www.paypal.com/sdk/js?client-id=AXPsjHSz9jJpvLxZcInFXlj1GFtu8bG52R2b4VEF7-DfExMXr7KK9ICq-I2NSerIRbFAJiwM7O-tLlGS&currency=EUR" data-sdk-integration-source="button-factory"></script>
<script>
  function initPayPalButton() {
    var shipping = 0;
    var itemOptions = document.querySelector("#smart-button-container #item-options");
    var quantity = parseInt();
    var quantitySelect = document.querySelector("#smart-button-container #quantitySelect");
    if (!isNaN(quantity)) {
      quantitySelect.style.visibility = "visible";
    }
    var orderDescription = 'Quota annuale';
    if(orderDescription === '') {
      orderDescription = 'Item';
    }

    paypal.Buttons({
      style: {
          shape: 'rect',
          color: 'gold',
          layout: 'horizontal',
          label: 'paypal',

      },
      createOrder: function(data, actions) {
        var selectedItemDescription = itemOptions.options[itemOptions.selectedIndex].value;
        var selectedItemPrice = parseFloat(itemOptions.options[itemOptions.selectedIndex].getAttribute("price"));
        var tax = (0 === 0) ? 0 : (selectedItemPrice * (parseFloat(0)/100));
        if(quantitySelect.options.length > 0) {
          quantity = parseInt(quantitySelect.options[quantitySelect.selectedIndex].value);
        } else {
          quantity = 1;
        }

        tax *= quantity;
        tax = Math.round(tax * 100) / 100;
        var priceTotal = quantity * selectedItemPrice + parseFloat(shipping) + tax;
        priceTotal = Math.round(priceTotal * 100) / 100;
        var itemTotalValue = Math.round((selectedItemPrice * quantity) * 100) / 100;

        return actions.order.create({
          purchase_units: [{
            description: orderDescription,
            amount: {
              currency_code: 'EUR',
              value: priceTotal,
              breakdown: {
                item_total: {
                  currency_code: 'EUR',
                  value: itemTotalValue,
                },
                shipping: {
                  currency_code: 'EUR',
                  value: shipping,
                },
                tax_total: {
                  currency_code: 'EUR',
                  value: tax,
                }
              }
            },
            items: [{
              name: selectedItemDescription,
              unit_amount: {
                currency_code: 'EUR',
                value: selectedItemPrice,
              },
              quantity: quantity
            }]
          }]
        });
      },
      onApprove: function(data, actions) {
          return actions.order.capture().then(function(details) {
              alert('Transaction completed by ' + details.payer.name.given_name + '!');
          });
      },
      onError: function(err) {
        console.log(err);
      },
    }).render('#paypal-button-container');
  }
  initPayPalButton();
</script>
