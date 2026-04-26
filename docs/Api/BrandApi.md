# Gethook\BrandApi



All URIs are relative to http://localhost:8080, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getBrandSettings()**](BrandApi.md#getBrandSettings) | **GET** /v1/brand-settings | Get brand settings |
| [**upsertBrandSettings()**](BrandApi.md#upsertBrandSettings) | **POST** /v1/brand-settings | Upsert brand settings |


## `getBrandSettings()`

```php
getBrandSettings(): \Gethook\Model\BrandSettings
```

Get brand settings

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\BrandApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getBrandSettings();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandApi->getBrandSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Gethook\Model\BrandSettings**](../Model/BrandSettings.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `upsertBrandSettings()`

```php
upsertBrandSettings($upsert_brand_settings_request): \Gethook\Model\BrandSettings
```

Upsert brand settings

Creates or replaces white-label brand settings for the account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\BrandApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$upsert_brand_settings_request = new \Gethook\Model\UpsertBrandSettingsRequest(); // \Gethook\Model\UpsertBrandSettingsRequest | Brand settings

try {
    $result = $apiInstance->upsertBrandSettings($upsert_brand_settings_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandApi->upsertBrandSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **upsert_brand_settings_request** | [**\Gethook\Model\UpsertBrandSettingsRequest**](../Model/UpsertBrandSettingsRequest.md)| Brand settings | |

### Return type

[**\Gethook\Model\BrandSettings**](../Model/BrandSettings.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
