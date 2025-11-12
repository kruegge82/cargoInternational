# kruegge82\cargoInternational\OrdersApi



All URIs are relative to https://app.spedition.de, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOrder()**](OrdersApi.md#createOrder) | **POST** /api/orders/create | Store new record |
| [**deleteOrder()**](OrdersApi.md#deleteOrder) | **DELETE** /api/orders/delete/{id} |  |
| [**destroyOrder()**](OrdersApi.md#destroyOrder) | **DELETE** /api/orders/destroy/{id} |  |
| [**getOrder()**](OrdersApi.md#getOrder) | **GET** /api/orders/details/{id} |  |
| [**listOrders()**](OrdersApi.md#listOrders) | **GET** /api/orders/index | List orders with pagination |
| [**listTrashedOrders()**](OrdersApi.md#listTrashedOrders) | **GET** /api/orders/trashed | List orders with pagination, including deleted |
| [**rateOrder()**](OrdersApi.md#rateOrder) | **POST** /api/orders/rate/{id} |  |
| [**restoreOrder()**](OrdersApi.md#restoreOrder) | **POST** /api/orders/restore/{id} |  |
| [**submitOrder()**](OrdersApi.md#submitOrder) | **POST** /api/orders/submit/{id} |  |
| [**updateOrder()**](OrdersApi.md#updateOrder) | **PATCH** /api/orders/update/{id} |  |


## `createOrder()`

```php
createOrder($create_order_request): array<string,mixed>
```

Store new record

Stores a new record.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_order_request = new \kruegge82\cargoInternational\Model\CreateOrderRequest(); // \kruegge82\cargoInternational\Model\CreateOrderRequest | Data to store

try {
    $result = $apiInstance->createOrder($create_order_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->createOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_order_request** | [**\kruegge82\cargoInternational\Model\CreateOrderRequest**](../Model/CreateOrderRequest.md)| Data to store | |

### Return type

**array<string,mixed>**

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteOrder()`

```php
deleteOrder($id): object
```



Delete single record

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the record

try {
    $result = $apiInstance->deleteOrder($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->deleteOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the record | |

### Return type

**object**

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `destroyOrder()`

```php
destroyOrder($id): object
```



Permanently delete a single record

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the record

try {
    $result = $apiInstance->destroyOrder($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->destroyOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the record | |

### Return type

**object**

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrder()`

```php
getOrder($id): array<string,mixed>
```



Lists single record

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Display specific record id

try {
    $result = $apiInstance->getOrder($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->getOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Display specific record id | |

### Return type

**array<string,mixed>**

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listOrders()`

```php
listOrders($per_page, $offset): \kruegge82\cargoInternational\Model\PaginatedResponse
```

List orders with pagination

Returns a list of orders.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records per page
$offset = 56; // int | The starting index for pagination

try {
    $result = $apiInstance->listOrders($per_page, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->listOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records per page | |
| **offset** | **int**| The starting index for pagination | [optional] |

### Return type

[**\kruegge82\cargoInternational\Model\PaginatedResponse**](../Model/PaginatedResponse.md)

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTrashedOrders()`

```php
listTrashedOrders($per_page, $offset): \kruegge82\cargoInternational\Model\PaginatedResponse
```

List orders with pagination, including deleted

Returns a list of orders.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records per page
$offset = 56; // int | The starting index for pagination

try {
    $result = $apiInstance->listTrashedOrders($per_page, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->listTrashedOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records per page | |
| **offset** | **int**| The starting index for pagination | [optional] |

### Return type

[**\kruegge82\cargoInternational\Model\PaginatedResponse**](../Model/PaginatedResponse.md)

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rateOrder()`

```php
rateOrder($id): array<string,mixed>
```



Query a price for an order, if supported by logistics partner

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Submit specific record id

try {
    $result = $apiInstance->rateOrder($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->rateOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Submit specific record id | |

### Return type

**array<string,mixed>**

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `restoreOrder()`

```php
restoreOrder($id): object
```



Restore single record that has been trashed prior

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the record

try {
    $result = $apiInstance->restoreOrder($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->restoreOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the record | |

### Return type

**object**

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `submitOrder()`

```php
submitOrder($id): array<string,mixed>
```



Submits order to logistics partner and creates shipping label

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Submit specific record id

try {
    $result = $apiInstance->submitOrder($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->submitOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Submit specific record id | |

### Return type

**array<string,mixed>**

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateOrder()`

```php
updateOrder($id, $update_order_request): object
```



Update a record

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the record
$update_order_request = new \kruegge82\cargoInternational\Model\UpdateOrderRequest(); // \kruegge82\cargoInternational\Model\UpdateOrderRequest | Data to update

try {
    $result = $apiInstance->updateOrder($id, $update_order_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->updateOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the record | |
| **update_order_request** | [**\kruegge82\cargoInternational\Model\UpdateOrderRequest**](../Model/UpdateOrderRequest.md)| Data to update | |

### Return type

**object**

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
