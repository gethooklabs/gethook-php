# Gethook\DestinationsApi



All URIs are relative to http://localhost:8080, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createDestination()**](DestinationsApi.md#createDestination) | **POST** /v1/destinations | Create destination |
| [**getDestination()**](DestinationsApi.md#getDestination) | **GET** /v1/destinations/{id} | Get destination |
| [**listDestinationPresets()**](DestinationsApi.md#listDestinationPresets) | **GET** /v1/destination-presets | List destination presets |
| [**listDestinations()**](DestinationsApi.md#listDestinations) | **GET** /v1/destinations | List destinations |
| [**rotateDestinationSecret()**](DestinationsApi.md#rotateDestinationSecret) | **POST** /v1/destinations/{id}/rotate-secret | Rotate destination signing secret |
| [**updateDestination()**](DestinationsApi.md#updateDestination) | **PATCH** /v1/destinations/{id} | Update destination |


## `createDestination()`

```php
createDestination($create_destination_request): \Gethook\Model\Destination
```

Create destination

Creates a new webhook delivery destination. The signing_secret is encrypted at rest and never returned.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\DestinationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_destination_request = new \Gethook\Model\CreateDestinationRequest(); // \Gethook\Model\CreateDestinationRequest | Destination config

try {
    $result = $apiInstance->createDestination($create_destination_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DestinationsApi->createDestination: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_destination_request** | [**\Gethook\Model\CreateDestinationRequest**](../Model/CreateDestinationRequest.md)| Destination config | |

### Return type

[**\Gethook\Model\Destination**](../Model/Destination.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDestination()`

```php
getDestination($id): \Gethook\Model\Destination
```

Get destination

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\DestinationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Destination UUID

try {
    $result = $apiInstance->getDestination($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DestinationsApi->getDestination: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Destination UUID | |

### Return type

[**\Gethook\Model\Destination**](../Model/Destination.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listDestinationPresets()`

```php
listDestinationPresets(): \Gethook\Model\DestinationPreset[]
```

List destination presets

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Gethook\Api\DestinationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listDestinationPresets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DestinationsApi->listDestinationPresets: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Gethook\Model\DestinationPreset[]**](../Model/DestinationPreset.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listDestinations()`

```php
listDestinations(): \Gethook\Model\Destination[]
```

List destinations

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\DestinationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listDestinations();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DestinationsApi->listDestinations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Gethook\Model\Destination[]**](../Model/Destination.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rotateDestinationSecret()`

```php
rotateDestinationSecret($id, $body): object
```

Rotate destination signing secret

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\DestinationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Destination UUID
$body = array('key' => new \stdClass); // object | New signing secret

try {
    $result = $apiInstance->rotateDestinationSecret($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DestinationsApi->rotateDestinationSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Destination UUID | |
| **body** | **object**| New signing secret | |

### Return type

**object**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDestination()`

```php
updateDestination($id, $update_destination_request): \Gethook\Model\Destination
```

Update destination

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\DestinationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Destination UUID
$update_destination_request = new \Gethook\Model\UpdateDestinationRequest(); // \Gethook\Model\UpdateDestinationRequest | Fields to update

try {
    $result = $apiInstance->updateDestination($id, $update_destination_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DestinationsApi->updateDestination: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Destination UUID | |
| **update_destination_request** | [**\Gethook\Model\UpdateDestinationRequest**](../Model/UpdateDestinationRequest.md)| Fields to update | |

### Return type

[**\Gethook\Model\Destination**](../Model/Destination.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
