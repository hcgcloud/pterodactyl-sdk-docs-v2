# List Locations <small>with Application API</small>
Get the collection of locations.

## Usage
``` php
<?php
	$pterodactyl->locations(int $page = 1);
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
		"short": "location-1",
		"long": "location-1",
		"createdAt": "2019-01-06T12:24:51+00:00",
		"updatedAt": "2019-10-29T12:25:05+00:00",
		"object": "location"
	}, {
		"id": 2,
		"short": "location-2",
		"long": "location-2",
		"createdAt": "2019-01-06T12:24:51+00:00",
		"updatedAt": "2019-10-29T12:25:05+00:00",
		"object": "location"
	}],
	"meta": {
		"pagination": {
			"total": 2,
			"count": 2,
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
	$locations = $pterodactyl->locations();
	print_r($locations);
?>
```