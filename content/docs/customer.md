---
order: 4
target: 'customer-end-point'
---
### Customer End-point

The customer endpoint allow you to create a customer token in order
for saving the customer credit card in Thawani servers and skipping the payment method when purchasing again 

__all the endpoints returns a promise__ 

#### Create  customer 
You can pass any thing is unique to the customer his email or phone number
```js 
await api.customer.create(customer_id)
```
#### Find Customer
By passing the customer token 
```js
await api.customer.find(customer_token); 
```
#### Find all customers 
```js
await api.customer.findAll(); 
```
or by passing a filter 
```js
await api.customer.findAll({
    skip:1, 
    limit:30
}); 
```
#### Remove customer 
```js 
await api.customer.remove(customer_token); 
```