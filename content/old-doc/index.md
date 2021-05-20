# ThawaniClient


This documentation is `before` the version 1.1.0  - you don't need to change the version if don't need but it's always better to be up-2-date 😃

## Documentation

please refer to Thawani [developer](https://developer.thawani.om/) Documentation

### install

`npm i thawani-node `

### usage

```javascript
const ThawaniClient = require("thawani-node");

const api = new ThawaniClient(
  "your_secret_key",
  "your_publishable_key",
  "dev|prod"
);

api
  .create_customer({
    client_customer_id: "Muhannad.alrisi@gmail.com",
  })
  .then((data) => {
    console.log(data);
  })
  .catch((err) => console.error(err));
```

#### Customer API

The following methods/functions are performing the customer endpoint API

##### Find a customer

Get a single customer by passing the the customer `token`

```javascript
api
  .find_customer((customer_token: string))
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

##### Get all customers

Get all customers please refer to the `Developer Docs`

```javascript
api
  .findAll_customers()
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

or

```javascript
api
  .findAll_customers({ skip: 1, limit: 10 })
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

##### Create customer

Create a new customer

```js
api
  .create_customer({
    client_customer_id: "Muhannad.alrisi@gmail.com",
  })
  .then((data) => {
    console.log(data);
  })
  .catch((err) => console.error(err));
```

##### Delete customer

To delete a customer

```js
api
  .delete_customer(customer_key)
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

#### Session API

The following functions/methods are related to Session endpoint
please refer to the developer docs

##### Create a session

Create a session to get the session token to use it later for the payment process

```js
api
  .create_session(payload)
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

#### Find a session

to get the information about a session by passing the `session id`

```js
api
  .find_session(session_id)
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

### Get all Sessions

To get all the sessions

```javascript
api
  .findAll_sessions()
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

or

```javascript
api
  .findAll_sessions({ skip: 1, limit: 10 })
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

##### Redirect to pay

pass the session id after a success creation to get the full path
for the payment API

```js
const full_redirect_uri = api.redirect(session_id);
```

##### Payments methods

the following API are related to the customer payments methods
please refer to the developer docs

##### Get customer payment method

To get customer payment method

```js
api
  .get_customer_payment({
    customerId: "customer_id",
  })
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

##### Remove customer payment method

To remove customer payment methods

```js
api
  .remove_customer_payment(card_token)
  .then((data) => console.log(data))
  .ctach((err) => console.error(err));
```
