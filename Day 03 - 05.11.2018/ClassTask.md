
# Task 

* Create this GET request with `curl`
```
    url: 'https://jsonplaceholder.typicode.com/posts/1'
    method: 'GET'
```

* Create this POST request with `curl`
```
    url: 'https://jsonplaceholder.typicode.com/posts'
    method: 'POST'
    headers: "Content-type": "application/json; charset=UTF-8"
    body:{
      title: 'foo',
      body: 'bar',
      userId: 1
    }
```


* Create this PUT request with `curl`
```
    url: 'https://jsonplaceholder.typicode.com/posts/1'
    method: 'PUT'
    headers: "Content-type": "application/json; charset=UTF-8"
    body:{
      id: 1,
      title: 'foo',
      body: 'bar',
      userId: 1
    }
```
  
* Create this DELETE request with `curl`
```
    url: 'https://jsonplaceholder.typicode.com/posts/1'
    method: 'DELETE'
```
   
