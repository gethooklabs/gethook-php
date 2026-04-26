# Gethook\IngestApi



All URIs are relative to http://localhost:8080, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**ingest()**](IngestApi.md#ingest) | **POST** /ingest/{token} | Ingest webhook event |


## `ingest()`

```php
ingest($token): \Gethook\Model\IngestAcceptedData
```

Ingest webhook event

Accepts an inbound webhook. The path token authenticates the source — no Bearer header required.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Gethook\Api\IngestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$token = 'token_example'; // string | Source path token (src_...)

try {
    $result = $apiInstance->ingest($token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IngestApi->ingest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token** | **string**| Source path token (src_...) | |

### Return type

[**\Gethook\Model\IngestAcceptedData**](../Model/IngestAcceptedData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
