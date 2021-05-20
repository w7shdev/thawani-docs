---
order: 2
target: 'Initialize'
---
### Initialize

#### Before we start 
Take a look in the [developer docs](https://developer.thawani.om/) so you have a better about the idea and the payload of each endpoint & you may not need this package if you are aiming to use only 1 or 2 end-points 

* __Note__ : This plugin just helps you to get the the integration fast
	* The package does not provide any helper function for formatting the payload
	* The package does not validate your payload 


 
#### Initialize

```js
const api = new ThawaniClient({
  secretKey: 'your_app_secret_key', 
  publishableKey : 'your_app_publishable_key',
  dev : true, // false to set it for production 
  filter: { // optional 
      skip: 1, 
      limit:10
  }
});
```
* `secretKey` - __required__ the secret key provided by Thawani 
* `publishableKey` - __require__ the publishable key provided by Thawani 
* `dev` - __required__ if this value set to `true` then the API will call the development end-points
* `filter` - __optional__ by  default the filter object has two keys `skip` and `limit` and they represent the page number and the result in each page 
    * `skip` - __optional__ page number default set to 1
    * `limit` - __optional__ number of result in each page default is 10 and the max is 50. 

