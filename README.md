# gethook-php — PHP SDK

PHP client for the [GetHook](https://gethook.io) Webhook Reliability Gateway API.

## Installation

```bash
composer require gethook/gethook-php
```

## Usage

```php
<?php
require_once 'vendor/autoload.php';

$config = Gethook\Configuration::getDefaultConfiguration()
    ->setHost('https://api.gethook.io')
    ->setApiKey('ApiKeyAuth', 'hk_your_api_key');

$client = new Gethook\Api\SourcesApi(new GuzzleHttp\Client(), $config);
$sources = $client->listSources();
print_r($sources);
```

## Documentation

Full API reference: https://docs.gethook.io/api-reference.html

## Development

This SDK is auto-generated from the OpenAPI spec via `make sync` in the main [gethook](https://github.com/gethook/gethook) repo.
