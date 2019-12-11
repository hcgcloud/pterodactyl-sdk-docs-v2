# Reinstall Server <small>with Application API</small>
Reinstall the given server.

## Usage
``` php
<?php
	$pterodactyl->reinstallServer($serverId);

	//For a server instance
	$server->reinstall();
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
		$pterodactyl->reinstallServer(14);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```

``` php
<?php
	try {
		$server = $pterodactyl->server(14);
		$server->reinstall();
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```