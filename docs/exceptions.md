# Exceptions

## AccessDeniedHttpException
This exception is thrown when the server returns `403`.

*Solution: Check the api key and permission.*

## FailedActionException
This exception is thrown when the server returns `400`.

*Solution: Check the response body.*

## NotFoundException
This exception is thrown when the server returns `404`.

*Solution: Check the response body.*

## InvaildApiTypeException
This exception is thrown when `API_TYPE` in instance creation is not set to `application` or `client`.

*Solution: Check API_TYPE in instance creation.*

## TimeoutException
This exception is thrown when the request is timeout.

*Solution: Check the connection between your server and panel.*

## ValidationException
This exception is thrown when the server returns `422`, the given data failed to pass validation.

### Solution

You can use code like the following to catch exceptions:

```php
<?php
	try {
		$servers = $pterodactyl->servers->create([
			//...
		]);
	} catch(\HCGCloud\Pterodactyl\Exceptions\ValidationException $e){
		print_r($e->errors());
	}
?>
```

By calling `$e->errors()` of a `ValidationException` will return you which parameter failed to pass the validation.