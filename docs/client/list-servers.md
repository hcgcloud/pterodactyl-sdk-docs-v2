# List Servers <small>with Account API</small>
Get the collection of servers for the authenticated user.

## Usage
``` php
<?php
	$pterodactyl->listServers(int $page = 1);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| page | The page number | |

## Returns

!!! note
    `id`, `externalId`, `node`, `suspended`, `pack`, `createdAt`, `updatedAt` will be always `null`, as they're not available with Account API.

``` json
{
	"data": [{
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
	}],
	"meta": {
		"pagination": {
			"total": 2,
			"count": 2,
			"per_page": 15,
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
	$server = $pterodactyl->listServers();
	print_r($server);
?>
```