# Gethook\PlatformApi



All URIs are relative to http://localhost:8080, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getPlatformStats()**](PlatformApi.md#getPlatformStats) | **GET** /v1/platform-stats | Public platform statistics |


## `getPlatformStats()`

```php
getPlatformStats(): \Gethook\Model\PlatformStats
```

Public platform statistics

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Gethook\Api\PlatformApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getPlatformStats();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlatformApi->getPlatformStats: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Gethook\Model\PlatformStats**](../Model/PlatformStats.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
