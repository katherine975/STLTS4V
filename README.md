curl -v -X POST https://api-m.sandbox.paypal.com/v2/checkout/orders \
-H "Content-Type: application/{
  "id": "p8rkxyx7zgkv8rk",
  "status": "CREATED",
  "links": [
    {
      "href": "https://api-m.paypal.com/v2/checkout/orders/p8rkxyx7zgkv8rk",
      "rel": "self",
      "method": "GET"
    },
    {
      "href": "https://www.paypal.com/checkoutnow?token=p8rkxyx7zgkv8rk",
      "rel": "approve",
      "method": "GET"
    },
    {
      "href": "https://api-m.paypal.com/v2/checkout/orders/p8rkxyx7zgkv8rk",
      "rel": "update",
      "method": "PATCH"
    },
    {
      "href": "https://api-m.paypal.com/v2/checkout/orders/p8rkxyx7zgkv8rk/capture",
      "rel": "capture",
      "method": "POST"
    }
  ]
}" \
-H "Authorization: Bearer Access-Token" \
-d '{
  "intent": "CAPTURE",
  "purchase_units": [
    {
      "amount": {
        "currency_code": "USD",
        "value": "100.00"
      }
    }
  ]
}'
