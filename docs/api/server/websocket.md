# Get Server Websocket <small>with Client API</small>
Get a server's websocket.

## Usage
``` php
<?php
	$pterodactyl->servers->websocket($serverId);
?>
```

## Parameters

!!! note
    The `serverID` is the identifier.

| Parameter | Description | Rules |
| - | - | - |
| serverId | The `identifier` of the server | |

## Returns

``` json
Response is unknown at this time.
```

## Example

``` php
<?php
	$websocket = $pterodactyl->servers->websocket(14);
	print_r($websocket);
?>
```
