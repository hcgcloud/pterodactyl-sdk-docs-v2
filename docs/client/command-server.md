# Command Server <small>with Account API</small>
Send a command to a given server.

## Usage
``` php
<?php
	$pterodactyl->commandServer($serverIdentifier, $command);

	//For a server instance
	$server->command($command);
?>
```

## Parameters

!!! note
    The `serverIdentifier` is the `identifier` of the server, not `id`, `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| serverIdentifier | The `identifier` of the server | |
| command | The command you want to send | |

## Returns
**None**

Throwing exception if failed.

## Example

``` php
<?php
	try {
		$pterodactyl->commandServer('76c59598', 'shutdown');
	} catch(Exception $e){
		print_r($e->getMessage());
	}
?>
```

``` php
<?php
	try {
		$server = $pterodactyl->getServer('76c59598');
		$server->command('shutdown');
	} catch(Exception $e){
		print_r($e->getMessage());
	}
?>
```