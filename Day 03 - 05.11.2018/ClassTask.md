
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
   
# Result

* GET request with `curl`
```
curl -v -X GET https://jsonplaceholder.typicode.com/posts/1
```

* POST request with `curl`
```
curl -v -X POST -H "Content-type: application/json" -d "{\"title\": \"foo\",\"body\": \"bar\",\"userId\": \"1\"}"  https://jsonplaceholder.typicode.com/posts 
```


* PUT request with `curl`
```
curl -v -X PUT -H "Content-type: application/json" -d "{\"title\": \"foo\",\"body\": \"bar\",\"userId\": \"1\", \"id\": \"1\"}" https://jsonplaceholder.typicode.com/posts/1
```
  
* DELETE request with `curl`
```
curl -v -X DELETE https://jsonplaceholder.typicode.com/posts/1
```
