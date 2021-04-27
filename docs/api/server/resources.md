# Get Server Resources <small>with Client API</small>
Get a server's resources.

## Usage
``` php
<?php
	$pterodactyl->servers->resources($serverId);
?>
```

## Parameters

!!! note
    The `serverID` is the identifier.

| Parameter | Description | Rules |
| - | - | - |
| serverId | The `identifier` of the server | |

## Returns

Returns a `stats`.

``` json
{
	"current_state": "starting",
	"is_suspended": false,
	"resources": {
	  "memory_bytes": 588701696,
	  "cpu_absolute": 0,
	  "disk_bytes": 130156361,
	  "network_rx_bytes": 694220,
	  "network_tx_bytes": 337090
	}
}
```

## Example

``` php
<?php
	$resources = $pterodactyl->servers->resources('066a878c');
	print_r($resources);
?>
```