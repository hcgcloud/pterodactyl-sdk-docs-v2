# Get Location <small>with Application API</small>
Get a location instance.

## Usage
``` php
<?php
	$pterodactyl->location($locationId);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| locationId | The `id` of the location | |

## Returns

Returns a `location instance`.

``` json
{
	"id": 1,
	"short": "location-1",
	"long": "location-1",
	"createdAt": "2019-01-06T12:24:51+00:00",
	"updatedAt": "2019-10-29T12:25:05+00:00",
	"object": "location"
}
```

## Example

``` php
<?php
	$location = $pterodactyl->location(1);
	print_r($location);
?>
```