# Update Server Build <small>with Application API</small>
Update an existing servers build.

!!! warning
    **This is still in BETA! This feature hasn't been tested yet!**
    
    **The documentation has not been completed**, you can [create PRs](https://github.com/hcgcloud/pterodactyl-sdk-docs) to improve this documentation.

## Usage
``` php
<?php
	$pterodactyl->updateBuild(int $serverId, array $data);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| data | The data to update the server | |
 
### data
| Parameter | Description | Rules |
| - | - | - |
| Allocation |  ID of primary Allocation | required&#124;int&#124;unique:servers |
| Limits.memory |  Memory / RAM | required&#124;int&#124;min:0 |
| Limits.swap |  Swap | required&#124;int&#124;min:0 |
| Limits.disk |  Disk  | required&#124;int&#124;min:0 |
| Limits.io |  IO | required&#124;int&#124;min:500 |
| Limits.memory |  CPU | required&#124;int&#124;min:0 |
| Feature_Limits.databases |  Databases | required&#124;int&#124;min:0 |
| Feature_Limits.allocations | Allocations | required&#124;int&#124;min:0 |
| Feature_Limits.backups | Backups | required&#124;int&#124;min:0 |



## Returns

Returns a `server instance`.

``` json
{
  "object": "server",
  "attributes": {
    "id": 5,
    "external_id": "RemoteID1",
    "uuid": "1a7ce997-259b-452e-8b4e-cecc464142ca",
    "identifier": "1a7ce997",
    "name": "Test",
    "description": "Pterodactyl Update Build",
    "suspended": false,
    "limits": {
      "memory": 512,
      "swap": 0,
      "disk": 200,
      "io": 500,
      "cpu": 0,
      "threads": null
    },
    "feature_limits": {
      "databases": 5,
      "allocations": 5,
      "backups": 2
    },
    "user": 1,
    "node": 1,
    "allocation": 1,
    "nest": 1,
    "egg": 5,
    "container": {
      "startup_command": "java -Xms128M -Xmx2014M -jar server.jar",
      "image": "quay.io\/pterodactyl\/core:java",
      "installed": true,
      "environment": {
        "SERVER_JARFILE": "server.jar",
        "VANILLA_VERSION": "latest",
        "STARTUP": "java -Xms128M -Xmx2048M -jar server.jar",
        "P_SERVER_LOCATION": "GB",
        "P_SERVER_UUID": "1a7ce997-259b-452e-8b4e-cecc464142ca",
        "P_SERVER_ALLOCATION_LIMIT": 5
      }
    },
    "updated_at": "2020-11-04T21:11:26+00:00",
    "created_at": "2019-12-23T06:46:27+00:00"
  }
}
```

## Example

``` php
<?php
	$server = $pterodactyl->updateBuild(5, [
        "allocation" => 1,
		"limits" => [
			"memory" => 256,
			"swap" => 0,
			"disk" => 1024,
			"io" => 500,
			"cpu" => 100
		],
		"feature_limits" => [
			"databases" => 1,
			"allocations" => 2, 
			"backups" => 3
		]
	]);
	print_r($server);
?>
```
