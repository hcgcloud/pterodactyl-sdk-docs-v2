# Get User by External Id <small>with Application API</small>
Get a user instance by external id.

## Usage
``` php
<?php
	$pterodactyl->userEx($externalId);
?>
```

## Parameters

!!! note
    The `externalId` is the `externalId` of the user, not `id` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| externalId | The `externalId` of the user | |

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
	"attributes": {
		"id": 1,
		"external_id": "1",
		"uuid": "c747ebbb-1989-413b-8eba-a49b74277c9f",
		"username": "user1",
		"email": "user1@email.com",
		"first_name": "user",
		"last_name": "123",
		"language": "zh",
		"root_admin": true,
		"2fa": true,
		"created_at": "2019-01-05T12:57:04+00:00",
		"updated_at": "2019-07-12T05:01:15+00:00"
	},
	"object": "user",
	"2fa": true
}
```

## Example

``` php
<?php
	$user = $pterodactyl->userEx(1);
	print_r($user);
?>
```