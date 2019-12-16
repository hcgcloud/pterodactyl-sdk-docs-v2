# Delete Allocation <small>with Application API</small>
Delete the given allocation.

## Usage
``` php
<?php
	$pterodactyl->deleteAllocation($nodeId, $allocationId);

	//For a node instance
	$node->deleteAllocation($allocationId);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| nodeId | The `id` of the node | |
| allocationId | The `id` of the allocation | |

## Returns
**None**

Throwing exception if failed.

## Example

``` php
<?php
	try {
		$pterodactyl->deleteAllocation(1, 3);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```

``` php
<?php
	try {
		$node = $pterodactyl->node(1);
		$node->deleteAllocation(3);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```