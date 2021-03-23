# Update Location <small>with Application API</small>
Update the given location.

## Usage
``` php
<?php
	$pterodactyl->updateLocation($locationId, array $data);

	//For a location instance
	$location->update(array $data);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| locationId | The `id` of the location | |
| data | The data to update location | |
 
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
	"short": "location-4",
	"long": "location-4",
	"createdAt": "2019-12-16T05:20:19+00:00",
	"updatedAt": "2019-12-16T05:23:16+00:00",
	"object": "location"
}
```

## Example

``` php
<?php
	$location = $pterodactyl->updateLocation(3, [
		'short' => 'location-4',
		'long' => 'location-4'
	]);
	print_r($location);
?>
```

``` php
<?php
	try {
		$location = $pterodactyl->location(3);
		$location->update([
			'short' => 'location-4',
			'long' => 'location-4'
		]);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```