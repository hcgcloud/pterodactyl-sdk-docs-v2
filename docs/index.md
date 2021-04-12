# Pterodactyl PHP SDK

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Total Downloads][ico-downloads]][link-downloads]
[![Software License][ico-license]](https://github.com/hcgcloud/pterodactyl-sdk/blob/master/LICENSE.md)
[![Chat on Discord][ico-chat]][link-chat]

Pterodactyl Panel PHP SDK(API wrapper).

!!! warning
    **This documentation is for `v2` version**, click [here](https://hcgcloud.github.io/pterodactyl-sdk-docs-v1/) for `v1` version.
    
    **The documentation has not been completed**, you can [create PRs](https://github.com/hcgcloud/pterodactyl-sdk-docs) to improve this documentation.

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
$pterodactyl = new \HCGCloud\Pterodactyl\Pterodactyl(BASE_URI, API_KEY, API_TYPE = 'application');
// API_TYPE can be set to application/client
```

Then you can call the apis.

## Usage

Please check `Api` from the navigation for more details.

## Support

You can get support by going to our [Discord server](https://discord.gg/5KnNVfv) or [submitting new issue](https://github.com/hcgcloud/pterodactyl-sdk/issues/new).

As a third-party API wrapper, We recommend you not asking for help elsewhere, or we may not be able to help you.

## License

`hcgcloud/pterodactyl-sdk` is licensed under the MIT License (MIT). Please see the
[license file](https://github.com/hcgcloud/pterodactyl-sdk/blob/master/LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/hcgcloud/pterodactyl-sdk.svg
[ico-license]: https://img.shields.io/badge/license-MIT-green.svg
[ico-downloads]: https://img.shields.io/packagist/dt/hcgcloud/pterodactyl-sdk.svg
[ico-chat]: https://img.shields.io/discord/609764930899673092

[link-packagist]: https://packagist.org/packages/hcgcloud/pterodactyl-sdk
[link-downloads]: https://packagist.org/packages/hcgcloud/pterodactyl-sdk
[link-chat]: https://discord.gg/5KnNVfv
