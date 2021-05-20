---
order: 8
target: 'Payment-Intent'
---

### Payment Intent

This endpoint to create a quick payments 

#### Create a payment 
```js
await api.paymentIntent.create(payload); 
```
#### Confirm a payment 
```js
await api.paymentIntent.confirm(paymentIntent_id); 
```
#### Cancel a payment 
```js
await api.paymentIntent.create(paymentIntent_id); 
```
#### Find a payment 
```js
await api.paymentIntent.find(paymentIntent_id); 
```
#### Find payment by reference
```js
await api.paymentIntent.findByReference(reference_id); 
```
#### Find all 
```js
await api.paymentIntent.findAll(); 
```
or by passing a `filter` as parameter
```js
await api.paymentIntent.findAll({
    skip:2,
    limit:10
}); 
``` 
