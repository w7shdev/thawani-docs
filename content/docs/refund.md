---
order: 7
target: 'Refund-API '
--- 
### Refund API 

Refund APi for getting refund to the client directly before the amount transferred  to your account

#### Create a refund 
```js 
await api.refund.create(payload);
```
#### Find a refund 
```js 
await api.refund.find();
```
#### Find all refunds 
```js 
await api.refund.findAll();
```
or by passing a `filter`
```js 
await api.refund.findAll({
    skip:2,
    limit:12
});
```

