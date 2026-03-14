# Gethook\AuthApi



All URIs are relative to http://localhost:8080, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**login()**](AuthApi.md#login) | **POST** /v1/auth/login | Login with email and password |
| [**register()**](AuthApi.md#register) | **POST** /v1/auth/register | Register with email and password |


## `login()`

```php
login($login_request): \Gethook\Model\AccountBootstrapData
```

Login with email and password

Authenticates with email/password and returns a fresh API key on success.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Gethook\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$login_request = new \Gethook\Model\LoginRequest(); // \Gethook\Model\LoginRequest | Login credentials

try {
    $result = $apiInstance->login($login_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->login: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **login_request** | [**\Gethook\Model\LoginRequest**](../Model/LoginRequest.md)| Login credentials | |

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

## `register()`

```php
register($register_request): \Gethook\Model\AccountBootstrapData
```

Register with email and password

Creates a new account with email/password credentials and returns a bootstrap API key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Gethook\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$register_request = new \Gethook\Model\RegisterRequest(); // \Gethook\Model\RegisterRequest | Registration details

try {
    $result = $apiInstance->register($register_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->register: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **register_request** | [**\Gethook\Model\RegisterRequest**](../Model/RegisterRequest.md)| Registration details | |

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
