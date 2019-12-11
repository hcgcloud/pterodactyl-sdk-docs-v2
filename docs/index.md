# Pterodactyl PHP SDK

Pterodactyl Panel API SDK for PHP (For Pterodactyl 0.7.x), a forked version from [@FruitBytes](https://github.com/FruitBytes).

## Quick start

To install the SDK in your project you need to require the package via [composer](http://getcomposer.org):

``` bash
composer require hcgcloud/pterodactyl-sdk
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

## Usage

Please check this documentation for more details.

*As our documentation is not finished yet, you can check out the [legacy readme file](https://github.com/hcgcloud/pterodactyl-sdk/blob/2b1759961a5a92eb95a3c9d3b045bd8410bdd43f/README.md) for all functions available of this SDK.*

## Support

You can get support by going to our [Discord server](https://discord.gg/5KnNVfv) or [submitting new issue](https://github.com/hcgcloud/pterodactyl-sdk/issues/new).

As a third-party API wrapper, We recommend you not asking for help elsewhere, or we may not be able to help you.

## License

`hcgcloud/pterodactyl-sdk` is licensed under the MIT License (MIT). Please see the
[license file](https://github.com/hcgcloud/pterodactyl-sdk/blob/master/LICENSE.md) for more information.
