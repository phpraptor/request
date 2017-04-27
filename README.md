Raptor Request
==============
Raptor Request is a light weight class to wrap the incoming HTTP request in one single object.

Documentation
-------------
### Installation
To install, just run the following composer command.
```
composer require phpraptor\request
```

### The Request Object
Here is an example to use the Raptor Request library.
```php
use Raptor\Request\Http

$request = new Http;
```

### Request Method
To get the incoming request method or the server verb, call the `method()` method.
```php
$request->method();

// Output
'POST'
```

### Query String Parameters
To get all the query string parameters ($_GET), call the `queries()` method.
```php
$request->queries();

// Output
[
    'hello' => 'world',
    'john' => 'doe'
]
```
If you want get a particular query string parameter, call the `query()` method and pass the required key as the argument.
```php
$request->query('john');

// Output
'doe'
```

### Request Body Parameters
To get all the request body parameters ($_POST), call the `params()` method.
```php
$request->params();

// Output
[
    'username' => 'phpraptor',
    'password' => 'johndoe'
]
```
If you want get a particular request body parameter, call the `param()` method and pass the required key as the argument.
```php
$request->param('username');

// Output
'phpraptor'
```

### License
This package is released under the [MIT License](https://github.com/phpraptor/request/blob/master/LICENSE).