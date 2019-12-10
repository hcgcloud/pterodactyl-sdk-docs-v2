# Pterodactyl PHP SDK

Pterodactyl Panel API SDK for PHP (For Pterodactyl 0.7.x), a forked version from [@FruitBytes](https://github.com/FruitBytes).

## Quick start

To install the SDK in your project you need to require the package via [composer](http://getcomposer.org):

``` bash
composer require hcgcloud/pterodactyl-sdk:dev-master
```

Then use Composer's autoload unless you are using a framework that support composer autoload:

``` php
require __DIR__.'/../vendor/autoload.php';
```

And finally create an instance of the SDK:

``` php
$pterodactyl = new \HCGCloud\Pterodactyl\Pterodactyl(API_KEY_HERE, BASE_URI_HERE);
```

Then you can call the apis.