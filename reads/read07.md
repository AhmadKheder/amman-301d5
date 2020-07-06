​
## SuperAgent
​
SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs. It also works with Node.js!
​
```node
 request
   .post('/api/pet')
   .send({ name: 'Manny', species: 'cat' })
   .set('X-API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(res => {
      alert('yay got ' + JSON.stringify(res.body));
   });
```

## Request basics
A request can be initiated by invoking the appropriate method on the request object, 
then calling `.then()` or `.end()` or `await()` to send the request. For example a simple GET request:

```node
 request
   .get('/search')
   .then(res = {
      // res.body, res.headers, res.status
   })
   .catch(err => {
      // err.message, err.response
   });
```

​**HTTP method may also be passed as a string:**
```node request('GET', '/search').then(success, failure);```


**Absolute URLs can be used. In web browsers absolute URLs work only if the server implements CORS.**


```node 
 request
   .get('https://example.com/search')
   .then(res => {

   });
   ```
__*Unix Domain Sockets:A Unix domain socket or IPC socket (inter-process communication socket) is a data communications endpoint for exchanging data between processes executing on the same host operating system. *__
**The Node client supports making requests to Unix Domain Sockets:**

```node 
 // pattern: https?+unix://SOCKET_PATH/REQUEST_PATH
//          Use `%2F` as `/` in SOCKET_PATH
try {
  const res = await request
    .get('http+unix://%2Fabsolute%2Fpath%2Fto%2Funix.sock/search');
  // res.body, res.headers, res.status
} catch(err) {
  // err.message, err.response
}
   ```
## **DELETE**, **HEAD**, **PATCH**, **POST**, and **PUT** requests can also be used, simply change the method name:

```node
request
  .head('/favicon.ico')
  .then(res => {

  });


```




