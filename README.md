# IQ Framework
>Just Another Framework
--- 

### Why You Should Using **IQ Framework** to make an API ?
 **Because**
 - Easy to use 
 - MVC 
 - Less than **1MB** file size !
 - Easy Routing System
 - and Much more.
---

# --- **Usage** ---

#### -- Routing
List of available methods
```php
Router::get();
Router::post();
Router::put();
Router::patch();
Router::delete();
Router::match();
```

Example: 
```php
Router::get('home', function() {
    return 'Home Page';
});
```

Route with parameters
```php
Route::get('hello/{name}', function($name) {
    return 'Hello' . $name;
});
```

Route with Controller
in `routes/web.php`
```php
Router::post('login', 'AuthController@login');
Router::get('user/{username}/profile', 'AuthController@showProfile'); // http://fake.com/login/testuser/profile
```
in `app/controllers/AuthController.php`
```php
namespace IqFramework\Controllers;

class AuthController {

	public function showProfile($username)
	{
		return $username; // testuser
	}
}
```

