# Update User <small>with Application API</small>
Update the given user.

## Usage
``` php
<?php
	$pterodactyl->updateUser($userId, array $data);

	//For a user instance
	$user->update(array $data);
?>
```

## Parameters

!!! note
    The `userId` is the `id` of the server, not `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| userId | The `id` of the user | |
| data | The data to update user | |
 
### data
| Parameter | Description | Rules |
| - | - | - |
| external_id |  External id | sometimes&#124;nullable&#124;string&#124;max:255&#124;unique:users,external_id |
| email | Email address | sometimes&#124;email&#124;unique:users,email |
| username | User name | required&#124;between:1,255&#124;unique:users,username |
| password | Password | sometimes&#124;nullable&#124;string |
| language | Language | sometimes&#124;string |
| root_admin | Whether root admin or not | sometimes&#124;boolean |
| first_name | First name | required&#124;string&#124;between:1,255 |
| last_name | Last name | required&#124;string&#124;between:1,255 |


## Returns

Returns a `user instance`.

``` json
{
	"id": 1,
	"externalId": "1",
	"uuid": "c747ebbb-1989-413b-8eba-a49b74277c9f",
	"username": "user1",
	"email": "user1@email.com",
	"firstName": "user",
	"lastName": "123",
	"language": "zh",
	"rootAdmin": true,
	"createdAt": "2019-01-05T12:57:04+00:00",
	"updatedAt": "2019-07-12T05:01:15+00:00",
	"object": "user",
	"2fa": true
}
```

## Example

``` php
<?php
	$user = $pterodactyl->updateUser([
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

``` php
<?php
	try {
		$user = $pterodactyl->user(29);
		$user->update([
			'email' => 'test@panel.com',
			'username' => 'testuser',
			'password' => 'thepassword',
			'language' => 'en',
			'root_admin' => false,
			'first_name' => 'Test',
			'last_name' => 'User'
		]);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```