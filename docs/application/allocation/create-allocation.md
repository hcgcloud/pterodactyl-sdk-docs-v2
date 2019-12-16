# Create Allocation <small>with Application API</small>
Create new allocation(s).

## Usage
``` php
<?php
	$pterodactyl->createAllocation($nodeId, array $data);
	
	//For a node instance
	$node->createAllocation(array $data);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| nodeId | The `id` of the node | |
| data | The data to create location | |
 
### data
| Parameter | Description | Rules |
| - | - | - |
| ip |  IP address | required&#124;string |
| alias | Alias name | sometimes&#124;nullable&#124;string&#124;max:255 |
| ports | Ports | required&#124;array |
| ports.* | Port | string |


## Returns
**None**

Throwing exception if failed.

## Example

``` php
<?php
	$pterodactyl->createAllocation(1, [
		'ip' => '123.123.123.123',
		'alias' => 'location-1.pterodactyl.panel',
		'ports' => [
			'51000',
			'51001',
			'51002'
		]
	]);
?>
```

``` php
<?php
	$node = $pterodactyl->node(1);
	$node->createAllocation([
		'ip' => '123.123.123.123',
		'alias' => 'location-1.pterodactyl.panel',
		'ports' => [
			'51000',
			'51001',
			'51002'
		]
	]);
?>
```
