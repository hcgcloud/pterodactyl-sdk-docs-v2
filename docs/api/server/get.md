# Get Server
Get a server instance.

## Usage
``` php
<?php
	$pterodactyl->servers->get($serverId, $query = []);
?>
```

## Parameters

!!! note
    For **Application API**, the `serverId` is the `id` of the server.
	
	For **Client API**, the `serverId` is the `identifier` of the server.

| Parameter | Description | Rules |
| - | - | - |
| serverId | The `id` or `identifier` of the server | |
| query | Additional query parameters | |

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
	}
}
```

## Example

``` php
<?php
	$server = $pterodactyl->servers->get(14);
	print_r($server);
?>
```