### Table of Contents
|#|Câu hỏi|
| --- | --- |
|  | [What is Routing?](#what-is-routing) |
|  | [How many types of routes are there?](#how-many-types-of-routes-are-there) |
|  | [What is web php?](#what-is-web-php) |
|  | [What is api php?](#what-is-api-php) |
|  | [What is channels php?](#what-is-channels-php) |
|  | [What is console-php?](#what-is-console-php) |
|  | [What is Controller?](#what-is-controller) |
|  | [What are Views?](#what-are-views) |
| | [What is a Model?](#what-is-a-model) |
|| [What is Request-Response?](#what-is-request-response) |

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

3. ### What is web php?

   web.php used for web routes. Like example.com/test

    ```
    Route::get('/test', function () {
        $path = storage_path() . "/app/json/options/docs.json";
        return view('skin/dev-wireframe', array('menu' => json_decode(file_get_contents($path), true)));
    });
    ```


**[⬆ Back to Top](#table-of-contents)**

4. ### What is api php?

   The place where we write API route for mobile and API usage. Like http://localhost:8080/api/test
    ```
    Route::get('/test', function () {
        $path = storage_path() . "/app/json/options/docs.json";
        return view('skin/dev-wireframe', array('menu' => json_decode(file_get_contents($path), true)));
    });
    ```
   **[⬆ Back to Top](#table-of-contents)**

5. ### What is channels php?

   It is used for broadcasting

**[⬆ Back to Top](#table-of-contents)**

6. ### What is console php?

   Used to give a name to console routes.

**[⬆ Back to Top](#table-of-contents)**


7. ### What is Controller?

   Controller is the place where we write the logic of the program. Placed in app/Http/Conrollers

    ```
    <?php namespace App\Http\Controllers;

    use App\Http\Controllers\Controller;

    class UserController extends Controller {

        /**
         * Show the profile for the given user.
         *
         * @param  int  $id
         * @return Response
         */
        public function showProfile($id)
        {
            return view('user.profile', ['user' => User::findOrFail($id)]);
        }

    }
    ```


**[⬆ Back to Top](#table-of-contents)**

8. ### What are Views?

Views is the fornt end of Laravel. Stored in `resources/views`.

    ```
    <html>
        <body>
            <h1>Hello, {{ $name }}</h1>
        </body>
    </html>
    ```


**[⬆ Back to Top](#table-of-contents)**

9. ### 	What is a Model?
   A model is where you write the database logic. Stored in `/app`

    <?php

    namespace App;

    use Illuminate\Database\Eloquent\Model;

    class Flight extends Model
    {
        //
    }

   **[⬆ Back to Top](#table-of-contents)**
    
10. ### What is Request-Response?

    When we type a URL, a request is sent to the server. The server goes from /public to bootstrap folder from which is goes to the routes file. The route files sends it the right controller/view.


**[⬆ Back to Top](#table-of-contents)**