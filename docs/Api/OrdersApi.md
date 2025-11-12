# kruegge82\cargoInternational\OrdersApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**a4dace2796ea4b9bbc26cf93c73ac5bf()**](OrdersApi.md#a4dace2796ea4b9bbc26cf93c73ac5bf) | **POST** /api/orders/submit/{id} |  |
| [**call0513395cd8422375c1a6e97d8f875e8e()**](OrdersApi.md#call0513395cd8422375c1a6e97d8f875e8e) | **GET** /api/orders/trashed | List orders with pagination, including deleted |
| [**call220692e5d32cd33591b288158ed08e81()**](OrdersApi.md#call220692e5d32cd33591b288158ed08e81) | **DELETE** /api/orders/delete/{id} |  |
| [**call26cb12e838cf1a4cf4af65d0eaf4ceb0()**](OrdersApi.md#call26cb12e838cf1a4cf4af65d0eaf4ceb0) | **DELETE** /api/orders/destroy/{id} |  |
| [**call29aaa3d442908d3a5a9a77902fa2285f()**](OrdersApi.md#call29aaa3d442908d3a5a9a77902fa2285f) | **POST** /api/orders/rate/{id} |  |
| [**call44093a5bd88f25dec2ab549f2efad341()**](OrdersApi.md#call44093a5bd88f25dec2ab549f2efad341) | **PATCH** /api/orders/update/{id} |  |
| [**call46849ce10119b18c6bb6888307a7a59a()**](OrdersApi.md#call46849ce10119b18c6bb6888307a7a59a) | **GET** /api/orders/index | List orders with pagination |
| [**call5d9463644f222f80d3a4e3564dc25243()**](OrdersApi.md#call5d9463644f222f80d3a4e3564dc25243) | **POST** /api/orders/restore/{id} |  |
| [**e56acd85f053dee29bb7af0d0338a243()**](OrdersApi.md#e56acd85f053dee29bb7af0d0338a243) | **GET** /api/orders/details/{id} |  |
| [**f649037b62fc19acd6bee704ff87a751()**](OrdersApi.md#f649037b62fc19acd6bee704ff87a751) | **POST** /orders/create | Store new record |


## `a4dace2796ea4b9bbc26cf93c73ac5bf()`

```php
a4dace2796ea4b9bbc26cf93c73ac5bf($id)
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
    $apiInstance->a4dace2796ea4b9bbc26cf93c73ac5bf($id);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->a4dace2796ea4b9bbc26cf93c73ac5bf: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Submit specific record id | |

### Return type

void (empty response body)

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `call0513395cd8422375c1a6e97d8f875e8e()`

```php
call0513395cd8422375c1a6e97d8f875e8e($per_page, $offset)
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
    $apiInstance->call0513395cd8422375c1a6e97d8f875e8e($per_page, $offset);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->call0513395cd8422375c1a6e97d8f875e8e: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records per page | |
| **offset** | **int**| The starting index for pagination | [optional] |

### Return type

void (empty response body)

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `call220692e5d32cd33591b288158ed08e81()`

```php
call220692e5d32cd33591b288158ed08e81($id): object
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
    $result = $apiInstance->call220692e5d32cd33591b288158ed08e81($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->call220692e5d32cd33591b288158ed08e81: ', $e->getMessage(), PHP_EOL;
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

## `call26cb12e838cf1a4cf4af65d0eaf4ceb0()`

```php
call26cb12e838cf1a4cf4af65d0eaf4ceb0($id): object
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
    $result = $apiInstance->call26cb12e838cf1a4cf4af65d0eaf4ceb0($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->call26cb12e838cf1a4cf4af65d0eaf4ceb0: ', $e->getMessage(), PHP_EOL;
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

## `call29aaa3d442908d3a5a9a77902fa2285f()`

```php
call29aaa3d442908d3a5a9a77902fa2285f($id)
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
    $apiInstance->call29aaa3d442908d3a5a9a77902fa2285f($id);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->call29aaa3d442908d3a5a9a77902fa2285f: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Submit specific record id | |

### Return type

void (empty response body)

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `call44093a5bd88f25dec2ab549f2efad341()`

```php
call44093a5bd88f25dec2ab549f2efad341($id, $body): object
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
$body = array('key' => new \stdClass); // object | Data to update

try {
    $result = $apiInstance->call44093a5bd88f25dec2ab549f2efad341($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->call44093a5bd88f25dec2ab549f2efad341: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the record | |
| **body** | **object**| Data to update | |

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

## `call46849ce10119b18c6bb6888307a7a59a()`

```php
call46849ce10119b18c6bb6888307a7a59a($per_page, $offset)
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
    $apiInstance->call46849ce10119b18c6bb6888307a7a59a($per_page, $offset);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->call46849ce10119b18c6bb6888307a7a59a: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records per page | |
| **offset** | **int**| The starting index for pagination | [optional] |

### Return type

void (empty response body)

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `call5d9463644f222f80d3a4e3564dc25243()`

```php
call5d9463644f222f80d3a4e3564dc25243($id): object
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
    $result = $apiInstance->call5d9463644f222f80d3a4e3564dc25243($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->call5d9463644f222f80d3a4e3564dc25243: ', $e->getMessage(), PHP_EOL;
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

## `e56acd85f053dee29bb7af0d0338a243()`

```php
e56acd85f053dee29bb7af0d0338a243($id)
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
    $apiInstance->e56acd85f053dee29bb7af0d0338a243($id);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->e56acd85f053dee29bb7af0d0338a243: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Display specific record id | |

### Return type

void (empty response body)

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `f649037b62fc19acd6bee704ff87a751()`

```php
f649037b62fc19acd6bee704ff87a751($f649037b62fc19acd6bee704ff87a751_request)
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
$f649037b62fc19acd6bee704ff87a751_request = new \kruegge82\cargoInternational\Model\F649037b62fc19acd6bee704ff87a751Request(); // \kruegge82\cargoInternational\Model\F649037b62fc19acd6bee704ff87a751Request | Data to store

try {
    $apiInstance->f649037b62fc19acd6bee704ff87a751($f649037b62fc19acd6bee704ff87a751_request);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->f649037b62fc19acd6bee704ff87a751: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **f649037b62fc19acd6bee704ff87a751_request** | [**\kruegge82\cargoInternational\Model\F649037b62fc19acd6bee704ff87a751Request**](../Model/F649037b62fc19acd6bee704ff87a751Request.md)| Data to store | |

### Return type

void (empty response body)

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
