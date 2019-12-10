# Get Server <small>with Account API</small>
Get the details of a given server.

## Usage
``` php
<?php
	$pterodactyl->getServer($serverIdentifier);
?>
```

## Parameters

!!! note
    The `serverIdentifier` is the `identifier` of the server, not `id`, `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| serverIdentifier | The `identifier` of the server | |

## Returns

Returns a `server instance`.

!!! note
    `id`, `externalId`, `node`, `suspended`, `pack`, `createdAt`, `updatedAt` will be always `null`, as they're not available with Account API.

``` json
{
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
}
```

## Example

``` php
<?php
	$server = $pterodactyl->getServer('76c59598');
	print_r($server);
?>
```