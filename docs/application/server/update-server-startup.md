# Update Server Startup <small>with Application API</small>
Update startup of the given server.

## Usage
``` php
<?php
	$pterodactyl->updateServerStartup($serverId, array $data);
	
	//For a server instance
	$server->updateStartup(array $data);
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
| startup | Startup command | required&#124;string |
| environment | Environment variables | present&#124;array |
| egg | Egg id | required&#124;exists:eggs,id |
| pack| Pack id | sometimes&#124;nullable&#124;numeric&#124;min:0 |
| image | Docker image | required&#124;string&#124;max:255 |
| skip_scripts | Skip egg scripts or not | present&#124;boolean |

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
	"attributes": {
		"id": 14,
		"external_id": null,
		"uuid": "76c59598-22df-4490-92bc-f6fb4a80e0c7",
		"identifier": "76c59598",
		"name": "server1",
		"description": "",
		"suspended": false,
		"limits": {
			"memory": 128,
			"swap": 0,
			"disk": 256,
			"io": 500,
			"cpu": 0
		},
		"feature_limits": {
			"databases": 0,
			"allocations": 0
		},
		"user": 1,
		"node": 1,
		"allocation": 55,
		"nest": 8,
		"egg": 20,
		"pack": null,
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
		"updated_at": "2019-08-05T09:36:13+00:00",
		"created_at": "2019-01-23T04:38:09+00:00",
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
	},
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
		"attributes": {
			"id": 55,
			"ip": "123.123.123.123",
			"alias": "node-1.pterodactyl.panel",
			"port": 50053,
			"assigned": true
		},
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
		$pterodactyl->updateServerStartup(14, [
			'startup' => './Jcmp-Server',
			'environment' => [
				'SERVER_AUTOUPDATE'
			],
			'egg' => 20,
			'pack' => null,
			'image' => 'hcgcloud/pterodactyl-jc2mp:latest',
			'skip_scripts' => false
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
		$server->updateStartup([
			'startup' => './Jcmp-Server',
			'environment' => [
				'SERVER_AUTOUPDATE'
			],
			'egg' => 20,
			'pack' => null,
			'image' => 'hcgcloud/pterodactyl-jc2mp:latest',
			'skip_scripts' => false
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
		$server->container['startup_command'] = './Jcmp-Server';
		$server->container['image'] = 'hcgcloud/pterodactyl-jc2mp:latest';
		$server->container['environment'] = [
			'SERVER_AUTOUPDATE'
		];
		$server->egg = 20;
		$server->updateStartup();
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```