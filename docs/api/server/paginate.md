# List Servers
Get a paginated collection of servers.

## Usage
``` php
<?php
	$pterodactyl->servers->paginate(int $page = 1, array $query = []);
?>
```

## Parameters

| Parameter | Description | Rules |
| - | - | - |
| page | The page number | |
| query | Additional query parameters | |

## Returns

```json
```

## Example

``` php
<?php
	$server = $pterodactyl->servers->get();
	print_r($server);
?>
```