# Delete User <small>with Application API</small>
Delete the given user.

## Usage
``` php
<?php
	$pterodactyl->deleteUser($userId);

	//For a user instance
	$user->delete();
?>
```

## Parameters

!!! note
    The `userId` is the `id` of the server, not `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| userId | The `id` of the user | |

## Returns
**None**

Throwing exception if failed.

## Example

``` php
<?php
	try {
		$pterodactyl->deleteUser(14);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```

``` php
<?php
	try {
		$user = $pterodactyl->user(14);
		$user->delete();
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```