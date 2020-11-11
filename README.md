### Stripe
---
https://dashboard.stripe.com/settings/user


https://stripe.com/partners/snipcart


https://github.com/stripe

###### [snipcart](https://github.com/takagotch/snipcart)
https://github.com/takagotch/snipcart

###### shopify lite
https://www.shopify.jp/lite

###### square
https://github.com/takagotch/square

###### Stripe Docs
https://stripe.com/docs/payments/accept-a-payment?integration=elements

######







```
connect

stripe
paypal
square
braintree
Mollie.com
Authorize.Net
```


```
// https://stripe.com/docs/payments/accept-a-payment?integration=elements
//
gem install stripe
vi Gemfile
+ gem 'stripe'
vi server.rb
+ Stripe.api_key = 'xxxxxxxxxxxxx'
+ intent = Stripe::PaymentIntent.create({
+   amount: 1099,
+   currency" 'jpy',
+   metadata: {integration_check: 'accept_a_payment'},
+ })
vi main.rb
+ get '/secret' do
+   intent = # PaymentIntent
+   {client_secret: intent.client_secret}.to_json
+ end
vi views/checkout.erb
+ <input id="card-name" type="text">
+ <!-- placeholder for Elements -->
+ <div id="card-element"></div>
+ <button id="card-button" data-secret="<%= @intent.client_secret %>">Submit Payment</button>
vi main.rb
+ get '' do
+   @intent = # PaymentIntent
+   erb :checkout
+ end
vi checkout.html
+ <script src="https://js.stripe.com/v3/"></stript>
+ <button i"checkout-button">Checkout</button>


```


```
```


```
```





