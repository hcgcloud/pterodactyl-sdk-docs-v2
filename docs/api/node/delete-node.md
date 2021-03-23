# Delete Node <small>with Application API</small>
Delete the given node.

## Usage
``` php
<?php
	$pterodactyl->deleteNode($nodeId);

	//For a node instance
	$node->delete();
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| nodeId | The `id` of the node | |

## Returns
**None**

Throwing exception if failed.

## Example

``` php
<?php
	try {
		$pterodactyl->deleteNode(3);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```

``` php
<?php
	try {
		$node = $pterodactyl->node(3);
		$node->delete();
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```