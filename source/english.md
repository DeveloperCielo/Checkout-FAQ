---
title: Perguntas frequêntes

toc_footers:
  - <a href='/Checkout-Cielo/english.html'>Cielo Checkout Guide</a>
  - <a href='/Checkout-Backoffice/'>Backoffice Cielo</a>

search: true
---

# Frequently Asked Questions (FAQ)

## What is the difference between the integration’s type used in CIELO CHECKOUT?

CIELO CHECKOUT uses integration via POST and you can configure it in two ways:

* **Integration via shopping cart** - used when there is a "shopping cart" to be sent, ie, the consumer's case navigate the website and choose one or more products to add to a cart and then finalize the transaction.
* **Integration via boleto** - used whenever there is no "shopping cart" in your store or when you want to associate a quick purchase/direct to a product. Each registered product generates a "buy button" only one that allows customization. Example: a hot site a promotion that takes the buyer directly to the payment step (Cielo's Checkout page).

## How do I create my button?

The button is created at the time of inclusion of a new product. To do this, go to   Backoffice Cielo's Checkout in Products/Sign Products menu.

## What information do I need to create the POST?

Data to be filled in POST are:

* Request data
* Cart
* Shipping data
* Consumer data

All information to assist in this process is in the Integration Manual Cielo Checkout.

## Can I send an e-mail marketing as a way of collecting?

Yes, through the integration via button you can send an e-mail marketing, or a charge by e-mail, adding to the HTML of the e-mail, the button for the product/service offered.

## What is the return URL?

To complete the purchase, the consumer has the option to return to the merchant's site or be directed to the page that the shopkeeper desired. The URL's function is automatically drives the consumer to the page defined in this option.

## What is the Notification URL?

At the end of a transaction, it sends a POST with all the sales' data to the URL's Notification, previously registered in the BackOffice. The notification POST is sent only when the transaction is completed, whether there is a change in the transaction status.

In this way the order data are updated in [Backoffice Cielo's Checkout](http://developercielo.github.io/Checkout-Backoffice/) and also in the backoffice of the store/platform.

## What is the URL's Change of Status?

It defines where the POST that indicates the change of status of a transaction will be sent, that is, when an application has changed their status, will be sending a POST to the URL's Change of Status, previously registered in the BackOffice. The POST of Change of Status doesn't contain the data of the shopping cart, only the identification data of the order.

## Where does register these URLs?

In [Backoffice Cielo Checkout](developercielo.github.io/Checkout-Backoffice/), at the Settings/Settings menu of the store.

## What is the difference between the CDOs error before and after the Checkout Cielo screen display?

* **Prior to the Checkout screen display** - Means that there was some gone wrong in sending the transaction, mandatory data may be missing or the format is invalid. Here the shopkeeper will always receive an email stating the error reason.
    * For these, a code is displayed (the same as the manual) within the application in Cielo Checkout Backoffice.
* **After the Checkout screen display (when the sale is finalized)** - It means there is an impediment for record that limits the sale. Things like blocked affiliation, error in the data saved in the registry or problems at own checkout.

## What is the relationship between the types of products and kinds of shipping?

The type of product being sold in Cielo Checkout influences directly the type of shipping and the information to be sent to the transaction processing.

The type of shipping to be used will depend on the type of product that your store sells. At Cielo's Checkout you can market 3 types of products:

* Physical Material
* Digital goods
* Services

The types of cargo that can be used are:

* Post offices
* Shipping Fixed
* Free shipping
* No Shipping (Withdrawal at hand)
* Without shipping charge (used for Digital Goods or Services)

Products (Physical Material category) require the qualification of some kind of shipping to be sent. In this case, the inclusion of information such as the weight of the product is required (CART_1_WEIGHT), Origin's CEP (Zip code)(CART_1_ZIPCODE) and Delivery CEP(Zip Code)(SHIPPING_ZIPCODE) to calculate shipping.

The categories "Digital Goods" or "Services" do not need this kind of information.

To understand the difference between the POST parameters regarding the shipping and product types, post compare examples below. For more information, visit [Checkout Integration of Cielo Manual](/Checkout-Cielo/english.html).

### Mandatory Parameters

|Physical material|Digital goods/Service|
|---------------|----------------|
|`MERCHANT_ID`|`MERCHANT_ID`|
|`ORDER_NUMBER`|`ORDER_NUMBER`|
|`SHIPPING_TYPE`: 1, 2 ou 3|`SHIPPING_TYPE`: 5|
|`SOFT_DESCRIPTOR|SOFT_DESCRIPTOR|
|`CART_1_NAME`|`CART_1_NAME`|
|`CART_1_UNITPRICE`|`CART_1_UNITPRICE`|
|`CART_1_QUANTITY`|`CART_1_QUANTITY`|
|`CART_1_WEIGHT`|`CART_1_TYPE`: 2 ou 3 **(Mandatory)**|
|`CART_1_ZIPCODE`|`CART_1_TYPE`: 1 **(Mandatory)**|
|`CUSTOMER_NAME`|`CUSTOMER_IDENTITY`|
|`SHIPPING_1_NAME`|`CUSTOMER_EMAIL`|
|`SHIPPING_1_PRICE`|`CUSTOMER_PHONE`|

## What is the test mode CHECKOUT CIELO?

It is a test environment, where you can simulate all actions without having to change their integration. It's a test environment where you can simulate sales and other test actions (such as cancellations, catches and chargebacks).

## How Cielo's Checkout test mode is activated?

In Cielo Checkout Backoffice, at Settings  Payments  Test Mode tab you can enable or disable the Test mode. When this mode is active, a wide red band appears at the top of all screens Cielo's Checkout (Checkout Backoffice and Payment screen). In the test mode the merchant or developer can transact testing and integration.

## Has the test mode some additional cost?

There are no fees. The test mode is available upon release from your account.
