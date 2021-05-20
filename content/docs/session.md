---
order: 3
target: 'sessions'
---
## sessions 

Sessions API are responsible of creating the payment and redirecting the user to Thawani checkout page

__note__ all the function are promised based.

#### Create  new session 
```js
 await api.session.create(payload);
```
#### Redirect to pay 
```js
const redirectFullURL = api.redirect(session_id);
```
#### get the session by id
```js
 await  api.sesssion.getSessionByID(session_id); // return a promise
```
#### get all the sessions 
```js
await api.session.findAll();
```
or you can pass `filter` object same as the class construct 
```js 
await api.session.findAll({
    skip :2, 
    limit: 20
});
```
#### Find session by reference 
```js 
await api.session.findSessionByReference(session_number); 
```
#### Find session by receipt number 
```js 
await api.session.findSessionByReceipt(receipt_number); 
```