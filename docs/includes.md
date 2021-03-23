# Includes

You may notice that some functions like `server()`, `user()` have a parameter called `$includes`, this can be used to query related data.

For example, to query all servers belongs to a user, you can use the following code:

```php
<?php
  $servers = $pterodactyl->users->get(1, [
    'include' => 'servers'
  ]);
  print_r($servers);
```

Here's a list of available includes.

!!! warning
    The list is not up to date, please check: [https://dashflo.net/docs/api/pterodactyl/v1/](https://dashflo.net/docs/api/pterodactyl/v1/).

## Includes

### Egg
 - servers
 - variables

### Location
 - nodes
 - servers

### Node
 - servers

### Server
 - allocations
 - databases
 - subusers

### User
 - servers