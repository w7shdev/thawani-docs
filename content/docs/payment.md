---
order: 5
target: 'payments'
---
### payments 

Payments endpoint shows the card type the customer uses

#### Find a payment 
```js
await api.payment.find(customer_token)
```

#### Remove a payment 
```js 
await api.payment.remove(card_token)
```
