# Create Location <small>with Application API</small>
Create a new location.

## Usage
``` php
<?php
	$pterodactyl->createLocation(array $data);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| data | The data to create location | |
 
### data
| Parameter | Description | Rules |
| - | - | - |
| short |  Short name | required&#124;string&#124;between:1,60&#124;unique:locations,short |
| long | Long name | required&#124;string&#124;between:1,255 |


## Returns

Returns a `location instance`.

``` json
{
	"id": 3,
	"short": "location-3",
	"long": "location-3",
	"attributes": {
		"id": 3,
		"short": "location-3",
		"long": "location-3",
		"updated_at": "2019-12-16T05:20:19+00:00",
		"created_at": "2019-12-16T05:20:19+00:00"
	},
	"createdAt": "2019-12-16T05:20:19+00:00",
	"updatedAt": "2019-12-16T05:20:19+00:00",
	"object": "location",
	"meta": {
		"resource": "https://pterodactyl.panel/api/application/locations/2"
	}
}
```

## Example

``` php
<?php
	$location = $pterodactyl->createLocation([
		'short' => 'location-3',
		'long' => 'location-3'
	]);
	print_r($location);
?>
```
