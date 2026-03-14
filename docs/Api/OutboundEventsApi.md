# Gethook\OutboundEventsApi



All URIs are relative to http://localhost:8080, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getOutboundEvent()**](OutboundEventsApi.md#getOutboundEvent) | **GET** /v1/outbound-events/{id} | Get outbound event |
| [**listOutboundEvents()**](OutboundEventsApi.md#listOutboundEvents) | **GET** /v1/outbound-events | List outbound events |
| [**publishOutboundEvent()**](OutboundEventsApi.md#publishOutboundEvent) | **POST** /v1/outbound-events | Publish outbound event |
| [**replayOutboundEvent()**](OutboundEventsApi.md#replayOutboundEvent) | **POST** /v1/outbound-events/{id}/replay | Replay outbound event |


## `getOutboundEvent()`

```php
getOutboundEvent($id): \Gethook\Model\EventDetailData
```

Get outbound event

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\OutboundEventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Event UUID

try {
    $result = $apiInstance->getOutboundEvent($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OutboundEventsApi->getOutboundEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Event UUID | |

### Return type

[**\Gethook\Model\EventDetailData**](../Model/EventDetailData.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listOutboundEvents()`

```php
listOutboundEvents($limit, $offset): \Gethook\Model\EventListData
```

List outbound events

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\OutboundEventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 56; // int | Max results (default 25, max 200)
$offset = 56; // int | Pagination offset

try {
    $result = $apiInstance->listOutboundEvents($limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OutboundEventsApi->listOutboundEvents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**| Max results (default 25, max 200) | [optional] |
| **offset** | **int**| Pagination offset | [optional] |

### Return type

[**\Gethook\Model\EventListData**](../Model/EventListData.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `publishOutboundEvent()`

```php
publishOutboundEvent($publish_outbound_event_request): \Gethook\Model\PublishOutboundData
```

Publish outbound event

Queues a new outbound event for delivery to all matching route destinations.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\OutboundEventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$publish_outbound_event_request = new \Gethook\Model\PublishOutboundEventRequest(); // \Gethook\Model\PublishOutboundEventRequest | Event payload

try {
    $result = $apiInstance->publishOutboundEvent($publish_outbound_event_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OutboundEventsApi->publishOutboundEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **publish_outbound_event_request** | [**\Gethook\Model\PublishOutboundEventRequest**](../Model/PublishOutboundEventRequest.md)| Event payload | |

### Return type

[**\Gethook\Model\PublishOutboundData**](../Model/PublishOutboundData.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `replayOutboundEvent()`

```php
replayOutboundEvent($id): \Gethook\Model\ReplayEventData
```

Replay outbound event

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Gethook\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gethook\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Gethook\Api\OutboundEventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Event UUID

try {
    $result = $apiInstance->replayOutboundEvent($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OutboundEventsApi->replayOutboundEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Event UUID | |

### Return type

[**\Gethook\Model\ReplayEventData**](../Model/ReplayEventData.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
