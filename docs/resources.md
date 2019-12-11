# Resources

When you use apis like `server()`, `node()`, it will return a resource instance.

Then you can call the functions of the instance, like `$server->update()`, `$node->delete()`, etc.

!!! note
    Be noticed that when you use functions like `update()`, the changes won't applied to the instance itself, so you should manually call the `get` api again to get the latest data.

Here's a list of available resource types.

## Type

### Allocation
The allocation resource.

### Egg
The egg resource.

### Nest
The nest resource.

### Node
The node resource.

#### Functions
``` php
<?php
  $node->delete();
  $node->update(array $data);
?>
```

### Server
The server resource.

#### Functions
``` php
<?php
  //Available with Application API
  $server->delete();
  $server->forceDelete();
  $server->suspend();
  $server->unsuspend();
  $server->updateDetails(array $data);
  $server->updateBuild(array $data);
  $server->updateStartup(array $data);
  $server->reinstall();
  $server->rebuild();
  
  //Available with Account API
  $server->power($action);
  $server->command($command);
?>
```

### Stats
The stats resource.

### User
The user resource.

#### Functions
``` php
<?php
  $user->delete();
  $user->update(array $data);
?>
```