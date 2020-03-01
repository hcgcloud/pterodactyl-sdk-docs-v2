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

Returns a `server instance`.

``` json
{
	"id": 14,
	"externalId": null,
	"uuid": "76c59598-22df-4490-92bc-f6fb4a80e0c7",
	"identifier": "76c59598",
	"node": 1,
	"name": "server1",
	"description": "",
	"suspended": false,
	"pack": null,
	"createdAt": "2019-01-23T04:38:09+00:00",
	"updatedAt": "2019-08-05T09:36:13+00:00",
	"limits": {
		"memory": 128,
		"swap": 0,
		"disk": 256,
		"io": 500,
		"cpu": 0
	},
	"allocations": [{
		"id": 55,
		"nodeId": null,
		"ip": "123.123.123.123",
		"ipAlias": null,
		"port": 50053,
		"serverId": null,
		"createdAt": null,
		"updatedAt": null,
		"object": "allocation",
		"alias": "node-1.pterodactyl.panel",
		"assigned": true
	}],
	"object": "server",
	"featureLimits": {
		"databases": 0,
		"allocations": 0
	},
	"user": 1,
	"allocation": 55,
	"nest": 8,
	"egg": 20,
	"container": {
		"startup_command": ".\/Jcmp-Server",
		"image": "hcgcloud\/pterodactyl-jc2mp:latest",
		"installed": true,
		"environment": {
			"SERVER_AUTOUPDATE": "0",
			"STARTUP": ".\/Jcmp-Server",
			"P_SERVER_LOCATION": "test",
			"P_SERVER_UUID": "76c59598-22df-4490-92bc-f6fb4a80e0c7"
		}
	},
	"relationships": {
		"allocations": {
			"object": "list",
			"data": [{
				"object": "allocation",
				"attributes": {
					"id": 55,
					"ip": "123.123.123.123",
					"alias": "node-1.pterodactyl.panel",
					"port": 50053,
					"assigned": true
				}
			}]
		}
	}
}
```

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