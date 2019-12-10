# List Servers <small>with Account API</small>
Get the collection of servers for the authenticated user.

## Usage
``` php
$pterodactyl->listServers();
```

## Parameters
*None*

## Returns

!!! note
    `id`, `externalId`, `node`, `suspended`, `pack`, `createdAt`, `updatedAt` will be always `null`, as they're not available with Account API.

``` json
[{
	"id": null,
	"externalId": null,
	"uuid": "76c59598-22df-4490-92bc-f6fb4a80e0c7",
	"identifier": "76c59598",
	"node": null,
	"name": "server1",
	"description": "",
	"suspended": null,
	"pack": null,
	"createdAt": null,
	"updatedAt": null,
	"attributes": {
		"server_owner": true,
		"identifier": "76c59598",
		"uuid": "76c59598-22df-4490-92bc-f6fb4a80e0c7",
		"name": "server1",
		"description": "",
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
		}
	},
	"limits": {
		"memory": 128,
		"swap": 0,
		"disk": 256,
		"io": 500,
		"cpu": 0
	},
	"allocations": [],
	"object": "server",
	"serverOwner": true,
	"featureLimits": {
		"databases": 0,
		"allocations": 0
	}
}, {
	"id": null,
	"externalId": null,
	"uuid": "6928f121-45bf-4f95-869a-eaebf02cd2a6",
	"identifier": "6928f121",
	"node": null,
	"name": "server2",
	"description": "",
	"suspended": null,
	"pack": null,
	"createdAt": null,
	"updatedAt": null,
	"attributes": {
		"server_owner": true,
		"identifier": "6928f121",
		"uuid": "6928f121-45bf-4f95-869a-eaebf02cd2a6",
		"name": "server2",
		"description": "",
		"limits": {
			"memory": 128,
			"swap": 0,
			"disk": 512,
			"io": 500,
			"cpu": 0
		},
		"feature_limits": {
			"databases": 0,
			"allocations": 0
		}
	},
	"limits": {
		"memory": 128,
		"swap": 0,
		"disk": 512,
		"io": 500,
		"cpu": 0
	},
	"allocations": [],
	"object": "server",
	"serverOwner": true,
	"featureLimits": {
		"databases": 0,
		"allocations": 0
	}
}]
```

## Example

``` php
<?php
	$server = $pterodactyl->listServers();
	print_r($server);
?>
```