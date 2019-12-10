# Power Server <small>with Account API</small>
Toggle the power on a given server.

## Usage
``` php
<?php
	$pterodactyl->powerServer($serverIdentifier, $action);

	//For a server instance
	$server->power($action);
?>
```

## Parameters

!!! note
    The `serverIdentifier` is the `identifier` of the server, not `id`, `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| serverIdentifier | The `identifier` of the server | |
| action | The action you want to send | in:start,stop,restart,kill |

## Returns
**None**

Throwing exception if failed.

## Example

``` php
<?php
	try {
		$pterodactyl->powerServer('76c59598', 'restart');
	} catch(Exception $e){
		print_r($e->getMessage());
	}
?>
```

``` php
<?php
	try {
		$server = $pterodactyl->getServer('76c59598');
		$server->power('restart');
	} catch(Exception $e){
		print_r($e->getMessage());
	}
?>
```