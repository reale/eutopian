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
      <div id="smart-button-container">
      <h2 id="paypal-payment">PayPal</h2>
      <form>
        <select class="custom-select" id="item-options">
          <option value="Individuals" price="50">Individuals - 50 EUR</option>
          <option value="Students" price="20">Students - 20 EUR</option>
          <option value="Startups, SMEs and business networks" price="150"> Startups, SMEs and business networks - 150 EUR</option>
          <option value="Non-profits" price="50">Non-profits - 50 EUR</option>
          <option value="Public bodies" price="50">Public bodies - 50 EUR</option>
          <option value="Large enterprises" price="500">Large enterprises - 500 EUR</option>
          </select>
        <select class="custom-select" style="visibility: hidden" id="quantitySelect"></select>
      </form>
      <div id="paypal-button-container"></div>
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
    var orderDescription = 'Annual fee';
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
