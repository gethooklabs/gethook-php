# gethook-php — PHP SDK

PHP client for the [GetHook](https://gethook.to) Webhook Reliability Gateway API.

## Installation

```bash
composer require gethook/gethook-php
```

## Usage

```php
<?php
require_once 'vendor/autoload.php';

$config = Gethook\Configuration::getDefaultConfiguration()
    ->setHost('https://api.gethook.to')
    ->setApiKey('ApiKeyAuth', 'hk_your_api_key');

$client = new Gethook\Api\SourcesApi(new GuzzleHttp\Client(), $config);
$sources = $client->listSources();
print_r($sources);
```

## Documentation

Full API reference: https://docs.gethook.to/reference

## Development

This SDK is auto-generated from the OpenAPI spec via `make sync` in the main [gethook](https://github.com/gethook/gethook) repo.
