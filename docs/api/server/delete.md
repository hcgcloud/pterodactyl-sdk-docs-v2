# Delete Server <small>with Application API</small>
Delete the given server.

## Usage
``` php
<?php
	$pterodactyl->deleteServer($serverId);

	//For a server instance
	$server->delete();
?>
```

## Parameters

!!! note
    The `serverId` is the `id` of the server, not `identifier`, `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| serverId | The `id` of the server | |

## Returns
**None**

Throwing exception if failed.

## Example

``` php
<?php
	try {
		$pterodactyl->deleteServer(14);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```

``` php
<?php
	try {
		$server = $pterodactyl->server(14);
		$server->delete();
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```