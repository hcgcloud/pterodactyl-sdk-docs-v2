# Create User <small>with Application API</small>
Create a new user.

## Usage
``` php
<?php
	$pterodactyl->createUser(array $data);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| data | The data to create user | |
 
### data
| Parameter | Description | Rules |
| - | - | - |
| external_id |  External id | sometimes&#124;nullable&#124;string&#124;max:255&#124;unique:users,external_id |
| email | Email address | sometimes&#124;email&#124;unique:users,email |
| username | User name | required&#124;between:1,255&#124;unique:users,username |
| password | Password | sometimes&#124;nullable&#124;string |
| language | Language | required&#124;string |
| root_admin | Whether root admin or not | boolean |
| first_name | First name | required&#124;string&#124;between:1,255 |
| last_name | Last name | required&#124;string&#124;between:1,255 |


## Returns

Returns a `user instance`.

``` json
{
	"id": 29,
	"externalId": null,
	"uuid": "ba8be618-e3e1-4495-aff3-6a2075e98fe3",
	"username": "testuser",
	"email": "test@panel.com",
	"firstName": "Test",
	"lastName": "User",
	"language": "en",
	"rootAdmin": false,
	"createdAt": "2019-12-11T10:47:19+00:00",
	"updatedAt": "2019-12-11T10:47:19+00:00",
	"object": "user",
	"meta": {
		"resource": "https:\/\/panel.pterodactyl\/api\/application\/users\/29"
	},
	"2fa": false
}
```

## Example

``` php
<?php
	$user = $pterodactyl->createUser([
		'email' => 'test@panel.com',
		'username' => 'testuser',
		'password' => 'thepassword',
		'language' => 'en',
		'root_admin' => false,
		'first_name' => 'Test',
		'last_name' => 'User'
	]);
	print_r($user);
?>
```
