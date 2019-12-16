# Delete Location <small>with Application API</small>
Delete the given location.

## Usage
``` php
<?php
	$pterodactyl->deleteLocation($locationId);

	//For a location instance
	$location->delete();
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| locationId | The `id` of the location | |

## Returns
**None**

Throwing exception if failed.

## Example

``` php
<?php
	try {
		$pterodactyl->deleteLocation(3);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```

``` php
<?php
	try {
		$location = $pterodactyl->location(3);
		$location->delete();
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```