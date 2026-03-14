# Gethook\AccountsApi



All URIs are relative to http://localhost:8080, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAccount()**](AccountsApi.md#createAccount) | **POST** /v1/accounts | Create account |


## `createAccount()`

```php
createAccount($create_account_request): \Gethook\Model\AccountBootstrapData
```

Create account

Creates a new account and returns a bootstrap API key. No authentication required.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Gethook\Api\AccountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_account_request = new \Gethook\Model\CreateAccountRequest(); // \Gethook\Model\CreateAccountRequest | Account name

try {
    $result = $apiInstance->createAccount($create_account_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountsApi->createAccount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_account_request** | [**\Gethook\Model\CreateAccountRequest**](../Model/CreateAccountRequest.md)| Account name | |

### Return type

[**\Gethook\Model\AccountBootstrapData**](../Model/AccountBootstrapData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
