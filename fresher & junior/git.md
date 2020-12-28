|#|Câu hỏi|
| --- | --- |
|1|[What is Routing?](#what-is-routing)|
|2|[How many types of routes are there?](#how-many-types-of-routes-are-there)|
|3|Câu 3|
|4|Câu 4|
|5|Câu 5|
|6|Câu 6|
|7|Câu 7|

---------

1. ### What is Routing?
When a user enters a URL, it gets send to a routes folder. web.php route is for web requests while api.php route is for API requests.

Below is an example get route from `routes/web.php`. You can call website.com/foo and it will bring the result.

  ```
  Route::get('foo', function () {
      return 'Hello World';
  });
  ```
**[⬆ Back to Top](#table-of-contents)**

2. ### How many types of routes are there?

There are four types of routes,

    A. web.php 
    
    B. api.php
    
    C. console.php
    
    D. broadcast.php

**[⬆ Back to Top](#table-of-contents)**

```php
$a = 3;
$b = $a++;
echo $b;
```