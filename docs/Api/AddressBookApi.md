# kruegge82\cargoInternational\AddressBookApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**c489ce3cefd3fd1fc942616eab9bb819()**](AddressBookApi.md#c489ce3cefd3fd1fc942616eab9bb819) | **GET** /api/addressbook/trashed | List records with pagination |
| [**call048b393249f9e4a7ba1074eb11be776b()**](AddressBookApi.md#call048b393249f9e4a7ba1074eb11be776b) | **DELETE** /api/addressbook/delete/{id} |  |
| [**call29e62d562eeb5644d97ca737c9558a68()**](AddressBookApi.md#call29e62d562eeb5644d97ca737c9558a68) | **GET** /api/addressbook/index | List records with pagination |
| [**call842e08c6da93ef68a4ec92a2de372624()**](AddressBookApi.md#call842e08c6da93ef68a4ec92a2de372624) | **PATCH** /api/addressbook/update/{id} |  |
| [**call8c231a8c867bb4e4c158dc745543f491()**](AddressBookApi.md#call8c231a8c867bb4e4c158dc745543f491) | **DELETE** /api/addressbook/destroy/{id} |  |
| [**d5e22cff88afd311443d76ca7e6b4d3a()**](AddressBookApi.md#d5e22cff88afd311443d76ca7e6b4d3a) | **POST** /api/addressbook/restore/{id} |  |
| [**db0828338113282bffb291676ce87860()**](AddressBookApi.md#db0828338113282bffb291676ce87860) | **POST** /api/addressbook/create | Store new record |
| [**fbf4e6189cd2bde77131813b38f16a20()**](AddressBookApi.md#fbf4e6189cd2bde77131813b38f16a20) | **GET** /api/addressbook/details/{id} |  |


## `c489ce3cefd3fd1fc942616eab9bb819()`

```php
c489ce3cefd3fd1fc942616eab9bb819($per_page, $page)
```

List records with pagination

Returns a list of records that are trashed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\AddressBookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records per page
$page = 56; // int | The starting page for pagination

try {
    $apiInstance->c489ce3cefd3fd1fc942616eab9bb819($per_page, $page);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->c489ce3cefd3fd1fc942616eab9bb819: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records per page | [optional] |
| **page** | **int**| The starting page for pagination | [optional] |

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

## `call048b393249f9e4a7ba1074eb11be776b()`

```php
call048b393249f9e4a7ba1074eb11be776b($id): object
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


$apiInstance = new kruegge82\cargoInternational\Api\AddressBookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the record

try {
    $result = $apiInstance->call048b393249f9e4a7ba1074eb11be776b($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->call048b393249f9e4a7ba1074eb11be776b: ', $e->getMessage(), PHP_EOL;
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

## `call29e62d562eeb5644d97ca737c9558a68()`

```php
call29e62d562eeb5644d97ca737c9558a68($per_page, $page)
```

List records with pagination

Returns a list of records

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: sanctum
$config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = kruegge82\cargoInternational\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new kruegge82\cargoInternational\Api\AddressBookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records per page
$page = 56; // int | The starting page for pagination

try {
    $apiInstance->call29e62d562eeb5644d97ca737c9558a68($per_page, $page);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->call29e62d562eeb5644d97ca737c9558a68: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records per page | [optional] |
| **page** | **int**| The starting page for pagination | [optional] |

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

## `call842e08c6da93ef68a4ec92a2de372624()`

```php
call842e08c6da93ef68a4ec92a2de372624($id, $_842e08c6da93ef68a4ec92a2de372624_request): object
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


$apiInstance = new kruegge82\cargoInternational\Api\AddressBookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the record
$_842e08c6da93ef68a4ec92a2de372624_request = new \kruegge82\cargoInternational\Model\842e08c6da93ef68a4ec92a2de372624Request(); // \kruegge82\cargoInternational\Model\842e08c6da93ef68a4ec92a2de372624Request | Data to store

try {
    $result = $apiInstance->call842e08c6da93ef68a4ec92a2de372624($id, $_842e08c6da93ef68a4ec92a2de372624_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->call842e08c6da93ef68a4ec92a2de372624: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the record | |
| **_842e08c6da93ef68a4ec92a2de372624_request** | [**\kruegge82\cargoInternational\Model\842e08c6da93ef68a4ec92a2de372624Request**](../Model/842e08c6da93ef68a4ec92a2de372624Request.md)| Data to store | |

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

## `call8c231a8c867bb4e4c158dc745543f491()`

```php
call8c231a8c867bb4e4c158dc745543f491($id): object
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


$apiInstance = new kruegge82\cargoInternational\Api\AddressBookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the record

try {
    $result = $apiInstance->call8c231a8c867bb4e4c158dc745543f491($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->call8c231a8c867bb4e4c158dc745543f491: ', $e->getMessage(), PHP_EOL;
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

## `d5e22cff88afd311443d76ca7e6b4d3a()`

```php
d5e22cff88afd311443d76ca7e6b4d3a($id): object
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


$apiInstance = new kruegge82\cargoInternational\Api\AddressBookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The ID of the record

try {
    $result = $apiInstance->d5e22cff88afd311443d76ca7e6b4d3a($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->d5e22cff88afd311443d76ca7e6b4d3a: ', $e->getMessage(), PHP_EOL;
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

## `db0828338113282bffb291676ce87860()`

```php
db0828338113282bffb291676ce87860($firstname, $lastname, $street, $zip, $city, $country, $phone, $email, $company, $department)
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


$apiInstance = new kruegge82\cargoInternational\Api\AddressBookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$firstname = 'firstname_example'; // string | The first name
$lastname = 'lastname_example'; // string | The last name
$street = 'street_example'; // string | Street & House number
$zip = 'zip_example'; // string | Zipcode
$city = 'city_example'; // string | City
$country = 'country_example'; // string | The 2 letter country code
$phone = 'phone_example'; // string | Phone number
$email = 'email_example'; // string | E-Mail address
$company = 'company_example'; // string | Company name
$department = 'department_example'; // string | Department name

try {
    $apiInstance->db0828338113282bffb291676ce87860($firstname, $lastname, $street, $zip, $city, $country, $phone, $email, $company, $department);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->db0828338113282bffb291676ce87860: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **firstname** | **string**| The first name | |
| **lastname** | **string**| The last name | |
| **street** | **string**| Street &amp; House number | |
| **zip** | **string**| Zipcode | |
| **city** | **string**| City | |
| **country** | **string**| The 2 letter country code | |
| **phone** | **string**| Phone number | |
| **email** | **string**| E-Mail address | |
| **company** | **string**| Company name | [optional] |
| **department** | **string**| Department name | [optional] |

### Return type

void (empty response body)

### Authorization

[sanctum](../../README.md#sanctum)

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `fbf4e6189cd2bde77131813b38f16a20()`

```php
fbf4e6189cd2bde77131813b38f16a20($id)
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


$apiInstance = new kruegge82\cargoInternational\Api\AddressBookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Display specific record id

try {
    $apiInstance->fbf4e6189cd2bde77131813b38f16a20($id);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->fbf4e6189cd2bde77131813b38f16a20: ', $e->getMessage(), PHP_EOL;
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
