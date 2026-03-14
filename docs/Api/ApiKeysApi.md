# Gethook\ApiKeysApi



All URIs are relative to http://localhost:8080, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createApiKey()**](ApiKeysApi.md#createApiKey) | **POST** /v1/api-keys | Create API key |
| [**deleteApiKey()**](ApiKeysApi.md#deleteApiKey) | **DELETE** /v1/api-keys/{id} | Revoke API key |
| [**listApiKeys()**](ApiKeysApi.md#listApiKeys) | **GET** /v1/api-keys | List API keys |


## `createApiKey()`

```php
createApiKey($create_api_key_request): \Gethook\Model\APIKeyWithSecret
```

Create API key

Creates a new API key for the authenticated account. The full key is only returned once.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_api_key_request = new \Gethook\Model\CreateAPIKeyRequest(); // \Gethook\Model\CreateAPIKeyRequest | Key name

try {
    $result = $apiInstance->createApiKey($create_api_key_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->createApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_api_key_request** | [**\Gethook\Model\CreateAPIKeyRequest**](../Model/CreateAPIKeyRequest.md)| Key name | |

### Return type

[**\Gethook\Model\APIKeyWithSecret**](../Model/APIKeyWithSecret.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteApiKey()`

```php
deleteApiKey($id)
```

Revoke API key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | API key UUID

try {
    $apiInstance->deleteApiKey($id);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->deleteApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| API key UUID | |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listApiKeys()`

```php
listApiKeys(): \Gethook\Model\APIKey[]
```

List API keys

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listApiKeys();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->listApiKeys: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Gethook\Model\APIKey[]**](../Model/APIKey.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
