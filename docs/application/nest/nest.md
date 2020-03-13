# Get nest <small>with Application API</small>
Get a nest instance.

## Usage
``` php
<?php
	$pterodactyl->nest($nestId, $includes = []);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| nestId | The `id` of the nest | |

## Returns

Returns a `nest instance`.

``` json
{
	"id": 1,
	"uuid": "9c212e4f-4dcb-445a-ae0a-2430a2eb81e5",
	"author": "support@pterodactyl.io",
	"name": "Minecraft",
	"description": "Minecraft - the classic game from Mojang. With support for Vanilla MC, Spigot, and many others!",
	"createdAt": "2019-01-05T12:56:46+00:00",
	"updatedAt": "2019-01-05T12:56:46+00:00",
	"object": "nest"
}
```

## Example

``` php
<?php
	$nest = $pterodactyl->nest(1);
	print_r($nest);
?>
```