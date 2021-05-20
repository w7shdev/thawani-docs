---
order: 1
target: 'Thawani-node'
---
### Thawani-node

Thawani node is a nodejs client for Thawani API 
this document is didicated for the pure purpose of 
migration of the plugin before the version `1.1.0`

if you have the early version before `1.1.0` the the class initialization will be this way 
The documentation of the previous version prior to version 1.1.0 is  <nuxt-link to="/old-version">here</nuxt-link>
```js
const api = new ThawaniClient(
  "your_secret_key",
  "your_publishable_key",
  "dev|prod"
);
```
and now it's like this 
```js
const api = new ThawaniClient({
  secretKey: 'your_app_secret_key', 
  publishableKey : 'your_app_publishable_key',
  dev : true // false to set it for production 
});
```

and this change can break your code or application 
