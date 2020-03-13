# Includes

You may notice that some functions like `server()`, `user()` have a parameter called `$includes`, this can be used to query related data.

For example, to query all servers belongs to a user, you can use the following code:

```php
  $servers = $pterodactyl->user(1, ['servers']);
  print_r($servers);
```

Here's a list of available includes, but it may not be a complete one.

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
 - subusers

### User
 - servers