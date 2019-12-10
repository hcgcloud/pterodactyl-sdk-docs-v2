# Get Server by External Id <small>with Application API</small>
Get a server instance by external id, including it's allocations.

## Usage
``` php
$pterodactyl->serverEx($externalId);
```

## Parameters

!!! note
    The `externalId` is the `externalId` of the server, not `identifier`, `id` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| externalId | The `externalId` of the server | |

## Returns

``` json
{
	"id": 14,
	"externalId": 11,
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
		"external_id": 11,
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
	$server = $pterodactyl->serverEx(11);
	print_r($server);
?>
```