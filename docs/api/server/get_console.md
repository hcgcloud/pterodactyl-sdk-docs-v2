# Get Server <small>with Client API</small>
Get a server's websocket.

## Usage
``` php
<?php
	$pterodactyl->websocket($serverId);
?>
```

## Parameters

!!! note
    The `serverId` is the `id` of the server, not `identifier`, `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| serverId | The `id` of the server | |

## Returns

Returns a `server websocket`.

``` json
Response is unknown at this time.
```

## Example

``` php
<?php
	$server = $pterodactyl->websocket(14);
	print_r($server);
?>
```