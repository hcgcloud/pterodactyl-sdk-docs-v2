# List Eggs <small>with Application API</small>
Get the collection of eggs of a nest.

## Usage
``` php
<?php
	$pterodactyl->eggs($nestId);
	
	//For a nest instance
	$nest->eggs();
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| nestId | The `id` of the nest | |

## Returns

``` json
[{
	"id": 14,
	"uuid": "c8422123-65e1-4e21-8097-a7b7356714b7",
	"nest": 4,
	"author": "support@pterodactyl.io",
	"description": "The only aim in Rust is to survive. To do this you will need to overcome struggles such as hunger, thirst and cold. Build a fire. Build a shelter. Kill animals for meat. Protect yourself from other players, and kill them for meat. Create alliances with other players and form a town. Do whatever it takes to survive.",
	"docker_image": null,
	"config": {
		"files": [],
		"startup": {
			"done": "Server startup complete",
			"userInteraction": []
		},
		"stop": "quit",
		"logs": {
			"custom": false,
			"location": "latest.log"
		},
		"extends": null
	},
	"startup": ".\/RustDedicated -batchmode +server.port {{SERVER_PORT}} +server.identity \"rust\" +rcon.port {{RCON_PORT}} +rcon.web true +server.hostname \\\"{{HOSTNAME}}\\\" +server.level \\\"{{LEVEL}}\\\" +server.description \\\"{{DESCRIPTION}}\\\" +server.url \\\"{{SERVER_URL}}\\\" +server.headerimage \\\"{{SERVER_IMG}}\\\" +server.worldsize \\\"{{WORLD_SIZE}}\\\" +server.seed \\\"{{WORLD_SEED}}\\\" +server.maxplayers {{MAX_PLAYERS}} +rcon.password \\\"{{RCON_PASS}}\\\" +server.saveinterval {{SAVEINTERVAL}} {{ADDITIONAL_ARGS}}",
	"script": {
		"privileged": true,
		"install": "apt update\r\napt -y --no-install-recommends install curl unzip lib32gcc1 ca-certificates\r\ncd \/tmp\r\ncurl -sSL -o steamcmd.tar.gz http:\/\/media.steampowered.com\/installer\/steamcmd_linux.tar.gz\r\n\r\nmkdir -p \/mnt\/server\/steam\r\ntar -xzvf steamcmd.tar.gz -C \/mnt\/server\/steam\r\ncd \/mnt\/server\/steam\r\nchown -R root:root \/mnt\r\n\r\nexport HOME=\/mnt\/server\r\n.\/steamcmd.sh +login anonymous +force_install_dir \/mnt\/server +app_update 258550 +quit\r\nmkdir -p \/mnt\/server\/.steam\/sdk32\r\ncp -v \/mnt\/server\/steam\/linux32\/steamclient.so \/mnt\/server\/.steam\/sdk32\/steamclient.so",
		"entry": "bash",
		"container": "ubuntu:16.04",
		"extends": null
	},
	"createdAt": "2019-01-05T12:56:46+00:00",
	"updatedAt": "2019-02-16T02:33:50+00:00",
	"object": "egg",
	"dockerImage": "quay.io\/pterodactyl\/core:rust"
}]
```

## Example

``` php
<?php
	$eggs = $pterodactyl->eggs(4);
	print_r($eggs);
?>
```

``` php
<?php
	$nest = $pterodactyl->nest(4);
	$eggs = $nest->eggs();
	print_r($eggs);
?>
```