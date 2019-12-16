# List Nodes <small>with Application API</small>
Get the collection of nodes.

## Usage
``` php
<?php
	$pterodactyl->nodes(int $page = 1);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| page | The page number | |

## Returns

``` json
{
	"data": [{
		"id": 1,
		"public": true,
		"name": "location-1",
		"description": "location-1",
		"locationId": 1,
		"fqdn": "location-1.pterodactyl.panel",
		"scheme": "https",
		"behindProxy": false,
		"maintenanceMode": false,
		"memory": 10240,
		"memoryOverallocate": 0,
		"disk": 102400,
		"diskOverallocate": 0,
		"uploadSize": 100,
		"daemonListen": 8084,
		"daemonSftp": 2022,
		"daemonBase": "\/srv\/daemon-data",
		"attributes": {
			"id": 1,
			"public": true,
			"name": "location-1",
			"description": "location-1",
			"location_id": 1,
			"fqdn": "location-1.pterodactyl.panel",
			"scheme": "https",
			"behind_proxy": false,
			"maintenance_mode": false,
			"memory": 10240,
			"memory_overallocate": 0,
			"disk": 102400,
			"disk_overallocate": 0,
			"upload_size": 100,
			"daemon_listen": 8084,
			"daemon_sftp": 2022,
			"daemon_base": "\/srv\/daemon-data",
			"created_at": "2019-01-06T12:40:08+00:00",
			"updated_at": "2019-10-29T12:24:28+00:00"
		},
		"createdAt": "2019-01-06T12:40:08+00:00",
		"updatedAt": "2019-10-29T12:24:28+00:00",
		"object": "node"
	}],
	"meta": {
		"pagination": {
			"total": 1,
			"count": 1,
			"per_page": 50,
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
	$nodes = $pterodactyl->nodes();
	print_r($nodes);
?>
```