---
order: 6
target: 'Payment-Transaction'
--- 
### Payment Transaction

Get the payment transaction details 

#### Find payment transaction 
```js
await api.paymentTransaction.find(payment_id); 
```
### Find All payments transactions 
```js
await api.paymentTransaction.findAll();
```
Or by passing a `filter` as a parameter 
```js
await api.paymentTransaction.findAll({
    skip:1, 
    limit:12
});
```

