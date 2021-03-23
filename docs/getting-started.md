# Getting started

## Installation

To install the SDK in your project you need to require the package via [composer](http://getcomposer.org):

``` bash
composer require hcgcloud/pterodactyl-sdk
```

Then use Composer's autoload unless you are using a framework that support composer autoload:

``` php
require __DIR__.'/../vendor/autoload.php';
```

And finally create an instance of the SDK, the `API_KEY` can be `Account API` or `Application API`, you can learn the difference [below](https://hcgcloud.github.io/pterodactyl-sdk-docs/getting-started/#type-of-api):

``` php
$pterodactyl = new \HCGCloud\Pterodactyl\Pterodactyl(API_KEY, BASE_URI, API_TYPE = 'application');
// API_TYPE can be set to application/client
```

or you can also use create an instance in this style:

``` php
use HCGCloud\Pterodactyl\Pterodactyl;
$pterodactyl = new Pterodactyl(API_KEY, BASE_URI, API_TYPE = 'application');
// API_TYPE can be set to application/client
```

## Usage

### Type of API
Before using other apis, you should know the difference between `Account API` and `Application API`.

#### Account API

!!! note
    You can find functions available for Account API in the `client` tab of the navigation.

Account API is for a single user of your panel, it can perform like `Send console command` and `Send power action` while Application API can't.

You can generate a key for an administrator account, then you can have the rights to control all servers.

Can be generated from: [https://yourpanel.url/account/api](https://yourpanel.url/account/api)

#### Application API
Application API is for your panel itself, it can perform like `Create Server` and `Create Node` while Account API can't.

Can be generated from: [https://yourpanel.url/admin/api](https://yourpanel.url/admin/api)

### Example
``` php
$servers = $pterodactyl->servers->paginate();
```

This will give you a paginated collection of servers that you have access to, each server is represented by an instance of `HCGCloud\Pterodactyl\Resources\Server`, this instance has multiple public
properties like `$name`, `$id`, `$owner`, `$memory`, and others.

You may also retrieve a single server using:

``` php
$server = $pterodactyl->servers->get(SERVER_ID_HERE);
```

**For other functions, you can find them from the navigation.**
