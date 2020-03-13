# Get User <small>with Application API</small>
Get a user instance.

## Usage
``` php
<?php
	$pterodactyl->user($userId, $includes = []);
?>
```

## Parameters

!!! note
    The `userId` is the `id` of the server, not `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| userId | The `id` of the user | |

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
	$user = $pterodactyl->user(1);
	print_r($user);
?>
```