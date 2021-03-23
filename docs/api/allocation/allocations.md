# List Allocations <small>with Application API</small>
Get the collection of allocations of a node.

## Usage
``` php
<?php
	$pterodactyl->allocations($nodeId, int $page = 1);

	//For a node instance
	$node->allocations(int $page = 1);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| nodeId | The `id` of the node | |
| page | The page number | |

## Returns

``` json
{
	"data": [{
		"id": 117,
		"ip": "123.123.123.123",
		"alias": "location-1.pterodactyl.panel",
		"port": 4202,
		"assigned": false,
		"object": "allocation"
	}, {
		"id": 103,
		"ip": "123.123.123.123",
		"alias": "location-1.pterodactyl.panel",
		"port": 5555,
		"assigned": false,
		"object": "allocation"
	}, {
		"id": 3,
		"ip": "123.123.123.123",
		"alias": "location-1.pterodactyl.panel",
		"port": 8888,
		"assigned": false,
		"object": "allocation"
	}],
	"meta": {
		"pagination": {
			"total": 3,
			"count": 3,
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
	$allocations = $pterodactyl->allocations(1);
	print_r($allocations);
?>
```

``` php
<?php
	$node = $pterodactyl->node(1);
	$allocations = $node->allocations();
	print_r($allocations);
?>
```