# Update Server Details <small>with Application API</small>
Update details of the given server.

## Usage
``` php
<?php
	$pterodactyl->updateServerDetails($serverId, array $data);
	
	//For a server instance
	$server->updateDetails(array $data);
?>
```

## Parameters

!!! note
    The `serverId` is the `id` of the server, not `identifier`, `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| serverId | The `id` of the server | |
| data | The data you want to update | |

### data
| Parameter | Description | Rules |
| - | - | - |
| external_id | External id | sometimes&#124;nullable&#124;string&#124;between:1,191&#124;unique:servers |
| name | Name | required&#124;string&#124;min:1&#124;max:255 |
| user | Server owner's user id | required&#124;integer&#124;exists:users,id |
| description | Description | sometimes&#124;nullable&#124;string |

## Returns
**None**

Throwing exception if failed.

## Example

``` php
<?php
	try {
		$pterodactyl->updateServerDetails(14, [
			'name' => 'newserver',
			'user' => 1,
			'description' => 'mynewdescription'
		]);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```

``` php
<?php
	try {
		$server = $pterodactyl->server(14);
		$server->updateDetails([
			'name' => 'newserver',
			'user' => 1,
			'description' => 'mynewdescription'
		]);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```