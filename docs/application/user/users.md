# List Users <small>with Application API</small>
Get the collection of users.

## Usage
``` php
<?php
	$pterodactyl->users(int $page = 1);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| page | The page number | |

## Returns

``` json
{
	"data": [{
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
			"firstName": "user",
			"lastName": "123",
			"language": "zh",
			"root_admin": true,
			"2fa": true,
			"created_at": "2019-01-05T12:57:04+00:00",
			"updated_at": "2019-07-12T05:01:15+00:00"
		},
		"object": "user",
		"2fa": true
	}, {
		"id": 2,
		"externalId": null,
		"uuid": "8ed41e98-e26c-4f3e-a022-0938865dd5b3",
		"username": "user2",
		"email": "user2@email.com",
		"firstName": "user",
		"lastName": "456",
		"language": "zh",
		"rootAdmin": false,
		"createdAt": "2019-01-08T07:55:43+00:00",
		"updatedAt": "2019-01-08T07:56:11+00:00",
		"attributes": {
			"id": 2,
			"external_id": null,
			"uuid": "8ed41e98-e26c-4f3e-a022-0938865dd5b3",
			"username": "user2",
			"email": "user2@email.com",
			"first_name": "user",
			"last_name": "456",
			"language": "zh",
			"root_admin": false,
			"2fa": false,
			"created_at": "2019-01-08T07:55:43+00:00",
			"updated_at": "2019-01-08T07:56:11+00:00"
		},
		"object": "user",
		"2fa": false
	}],
	"meta": {
		"pagination": {
			"total": 2,
			"count": 2,
			"per_page": 50,
			"current_page": 1,
			"total_pages": 1,
			"links": []
		}
	}
}
```

## Example

``` php
<?php
	$users = $pterodactyl->users();
	print_r($users);
?>
```