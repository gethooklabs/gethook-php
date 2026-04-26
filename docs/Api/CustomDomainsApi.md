# Gethook\CustomDomainsApi



All URIs are relative to http://localhost:8080, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCustomDomain()**](CustomDomainsApi.md#createCustomDomain) | **POST** /v1/custom-domains | Create custom domain |
| [**listCustomDomains()**](CustomDomainsApi.md#listCustomDomains) | **GET** /v1/custom-domains | List custom domains |


## `createCustomDomain()`

```php
createCustomDomain($create_custom_domain_request): \Gethook\Model\CustomDomain
```

Create custom domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\CustomDomainsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_custom_domain_request = new \Gethook\Model\CreateCustomDomainRequest(); // \Gethook\Model\CreateCustomDomainRequest | Domain details

try {
    $result = $apiInstance->createCustomDomain($create_custom_domain_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomDomainsApi->createCustomDomain: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_custom_domain_request** | [**\Gethook\Model\CreateCustomDomainRequest**](../Model/CreateCustomDomainRequest.md)| Domain details | |

### Return type

[**\Gethook\Model\CustomDomain**](../Model/CustomDomain.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCustomDomains()`

```php
listCustomDomains(): \Gethook\Model\CustomDomain[]
```

List custom domains

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\CustomDomainsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listCustomDomains();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomDomainsApi->listCustomDomains: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Gethook\Model\CustomDomain[]**](../Model/CustomDomain.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
