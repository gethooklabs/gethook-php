# Gethook\RoutesApi



All URIs are relative to http://localhost:8080, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createRoute()**](RoutesApi.md#createRoute) | **POST** /v1/routes | Create route |
| [**listRoutes()**](RoutesApi.md#listRoutes) | **GET** /v1/routes | List routes |


## `createRoute()`

```php
createRoute($create_route_request): \Gethook\Model\Route
```

Create route

Creates a routing rule that forwards matching events from a source to a destination.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\RoutesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_route_request = new \Gethook\Model\CreateRouteRequest(); // \Gethook\Model\CreateRouteRequest | Route config

try {
    $result = $apiInstance->createRoute($create_route_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoutesApi->createRoute: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_route_request** | [**\Gethook\Model\CreateRouteRequest**](../Model/CreateRouteRequest.md)| Route config | |

### Return type

[**\Gethook\Model\Route**](../Model/Route.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listRoutes()`

```php
listRoutes(): \Gethook\Model\Route[]
```

List routes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\RoutesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listRoutes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoutesApi->listRoutes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Gethook\Model\Route[]**](../Model/Route.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
