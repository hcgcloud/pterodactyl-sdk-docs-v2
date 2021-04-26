# Get Server Resources <small>with Client API</small>
Get a server's websocket.

## Usage
``` php
<?php
	$pterodactyl->resources($serverId);
?>
```

## Parameters

!!! note
    The `serverID` is the identifier.

| Parameter | Description | Rules |
| - | - | - |
| serverId | The `id` of the server | |

## Returns

Returns a `servers resource usage`.

``` json
{
  "object": "stats",
  "attributes": {
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
	$server = $pterodactyl->resources('066a878c');
	print_r($server);
?>
```