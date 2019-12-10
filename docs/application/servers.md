# List Servers <small>with Application API</small>
Get the collection of servers.

## Usage
``` php
<?php
	$pterodactyl->servers(int $page = 1);
?>
```

## Parameters
*None*

## Returns

``` json
{
	"data": [{
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
			"created_at": "2019-01-23T04:38:09+00:00"
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
	}, {
		"id": 20,
		"externalId": null,
		"uuid": "6928f121-45bf-4f95-869a-eaebf02cd2a6",
		"identifier": "6928f121",
		"node": 1,
		"name": "server2",
		"description": "",
		"suspended": false,
		"pack": null,
		"createdAt": "2019-01-23T11:18:57+00:00",
		"updatedAt": "2019-07-28T06:35:00+00:00",
		"attributes": {
			"id": 20,
			"external_id": null,
			"uuid": "6928f121-45bf-4f95-869a-eaebf02cd2a6",
			"identifier": "6928f121",
			"name": "server2",
			"description": "",
			"suspended": false,
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
			},
			"user": 1,
			"node": 1,
			"allocation": 73,
			"nest": 9,
			"egg": 21,
			"pack": null,
			"container": {
				"startup_command": ".\/Server",
				"image": "hcgcloud\/pterodactyl-jc3mp:latest",
				"installed": true,
				"environment": {
					"SERVER_AUTOUPDATE": "0",
					"QUERY_PORT": "50072",
					"HTTP_PORT": "50073",
					"STARTUP": ".\/Server",
					"P_SERVER_LOCATION": "test",
					"P_SERVER_UUID": "6928f121-45bf-4f95-869a-eaebf02cd2a6"
				}
			},
			"updated_at": "2019-07-28T06:35:00+00:00",
			"created_at": "2019-01-23T11:18:57+00:00"
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
		"featureLimits": {
			"databases": 0,
			"allocations": 0
		},
		"user": 1,
		"allocation": 73,
		"nest": 9,
		"egg": 21,
		"container": {
			"startup_command": ".\/Server",
			"image": "hcgcloud\/pterodactyl-jc3mp:latest",
			"installed": true,
			"environment": {
				"SERVER_AUTOUPDATE": "0",
				"QUERY_PORT": "50072",
				"HTTP_PORT": "50073",
				"STARTUP": ".\/Server",
				"P_SERVER_LOCATION": "test",
				"P_SERVER_UUID": "6928f121-45bf-4f95-869a-eaebf02cd2a6"
			}
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
	$server = $pterodactyl->servers();
	print_r($server);
?>
```