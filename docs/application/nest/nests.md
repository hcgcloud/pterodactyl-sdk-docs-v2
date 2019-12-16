# List Nests <small>with Application API</small>
Get the collection of nests.

## Usage
``` php
<?php
	$pterodactyl->nests(int $page = 1);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| page | The page number | |

## Returns

``` json
{
	"data": [{
		"id": 1,
		"uuid": "9c212e4f-4dcb-445a-ae0a-2430a2eb81e5",
		"author": "support@pterodactyl.io",
		"name": "Minecraft",
		"description": "Minecraft - the classic game from Mojang. With support for Vanilla MC, Spigot, and many others!",
		"attributes": {
			"id": 1,
			"uuid": "9c212e4f-4dcb-445a-ae0a-2430a2eb81e5",
			"author": "support@pterodactyl.io",
			"name": "Minecraft",
			"description": "Minecraft - the classic game from Mojang. With support for Vanilla MC, Spigot, and many others!",
			"created_at": "2019-01-05T12:56:46+00:00",
			"updated_at": "2019-01-05T12:56:46+00:00"
		},
		"createdAt": "2019-01-05T12:56:46+00:00",
		"updatedAt": "2019-01-05T12:56:46+00:00",
		"object": "nest"
	}, {
		"id": 2,
		"uuid": "29063c0f-36f0-4e64-84fb-f163c3e98892",
		"author": "support@pterodactyl.io",
		"name": "Source Engine",
		"description": "Includes support for most Source Dedicated Server games.",
		"attributes": {
			"id": 2,
			"uuid": "29063c0f-36f0-4e64-84fb-f163c3e98892",
			"author": "support@pterodactyl.io",
			"name": "Source Engine",
			"description": "Includes support for most Source Dedicated Server games.",
			"created_at": "2019-01-05T12:56:46+00:00",
			"updated_at": "2019-01-05T12:56:46+00:00"
		},
		"createdAt": "2019-01-05T12:56:46+00:00",
		"updatedAt": "2019-01-05T12:56:46+00:00",
		"object": "nest"
	}, {
		"id": 3,
		"uuid": "1a4aa82d-5368-4e04-9b8d-1ee77d4ec414",
		"author": "support@pterodactyl.io",
		"name": "Voice Servers",
		"description": "Voice servers such as Mumble and Teamspeak 3.",
		"attributes": {
			"id": 3,
			"uuid": "1a4aa82d-5368-4e04-9b8d-1ee77d4ec414",
			"author": "support@pterodactyl.io",
			"name": "Voice Servers",
			"description": "Voice servers such as Mumble and Teamspeak 3.",
			"created_at": "2019-01-05T12:56:46+00:00",
			"updated_at": "2019-01-05T12:56:46+00:00"
		},
		"createdAt": "2019-01-05T12:56:46+00:00",
		"updatedAt": "2019-01-05T12:56:46+00:00",
		"object": "nest"
	}, {
		"id": 4,
		"uuid": "43017190-4513-48c7-894a-cb058bb4ee07",
		"author": "support@pterodactyl.io",
		"name": "Rust",
		"description": "Rust - A game where you must fight to survive.",
		"attributes": {
			"id": 4,
			"uuid": "43017190-4513-48c7-894a-cb058bb4ee07",
			"author": "support@pterodactyl.io",
			"name": "Rust",
			"description": "Rust - A game where you must fight to survive.",
			"created_at": "2019-01-05T12:56:46+00:00",
			"updated_at": "2019-01-05T12:56:46+00:00"
		},
		"createdAt": "2019-01-05T12:56:46+00:00",
		"updatedAt": "2019-01-05T12:56:46+00:00",
		"object": "nest"
	}],
	"meta": {
		"pagination": {
			"total": 4,
			"count": 4,
			"per_page": 50,
			"current_page": 1,
			"total_pages": 1,
			"links": []
		}
	}
}
```

## Example

``` php
<?php
	$nests = $pterodactyl->nests();
	print_r($nests);
?>
```