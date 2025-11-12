# kruegge82\cargoInternational\AddressBookApi



All URIs are relative to https://app.spedition.de, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAddressbook()**](AddressBookApi.md#createAddressbook) | **POST** /api/addressbook/create | Store new record |
| [**deleteAddressbook()**](AddressBookApi.md#deleteAddressbook) | **DELETE** /api/addressbook/delete/{id} |  |
| [**destroyAddressbook()**](AddressBookApi.md#destroyAddressbook) | **DELETE** /api/addressbook/destroy/{id} |  |
| [**getAddressbook()**](AddressBookApi.md#getAddressbook) | **GET** /api/addressbook/details/{id} |  |
| [**listAddressbook()**](AddressBookApi.md#listAddressbook) | **GET** /api/addressbook/index | List records with pagination |
| [**listTrashedAddressbook()**](AddressBookApi.md#listTrashedAddressbook) | **GET** /api/addressbook/trashed | List records with pagination |
| [**restoreAddressbook()**](AddressBookApi.md#restoreAddressbook) | **POST** /api/addressbook/restore/{id} |  |
| [**updateAddressbook()**](AddressBookApi.md#updateAddressbook) | **PATCH** /api/addressbook/update/{id} |  |


## `createAddressbook()`

```php
createAddressbook($firstname, $lastname, $street, $zip, $city, $country, $phone, $email, $company, $department)
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
    $apiInstance->createAddressbook($firstname, $lastname, $street, $zip, $city, $country, $phone, $email, $company, $department);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->createAddressbook: ', $e->getMessage(), PHP_EOL;
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

## `deleteAddressbook()`

```php
deleteAddressbook($id): object
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
    $result = $apiInstance->deleteAddressbook($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->deleteAddressbook: ', $e->getMessage(), PHP_EOL;
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

## `destroyAddressbook()`

```php
destroyAddressbook($id): object
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
    $result = $apiInstance->destroyAddressbook($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->destroyAddressbook: ', $e->getMessage(), PHP_EOL;
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

## `getAddressbook()`

```php
getAddressbook($id)
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
    $apiInstance->getAddressbook($id);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->getAddressbook: ', $e->getMessage(), PHP_EOL;
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

## `listAddressbook()`

```php
listAddressbook($per_page, $page)
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
    $apiInstance->listAddressbook($per_page, $page);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->listAddressbook: ', $e->getMessage(), PHP_EOL;
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

## `listTrashedAddressbook()`

```php
listTrashedAddressbook($per_page, $page)
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
    $apiInstance->listTrashedAddressbook($per_page, $page);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->listTrashedAddressbook: ', $e->getMessage(), PHP_EOL;
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

## `restoreAddressbook()`

```php
restoreAddressbook($id): object
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
    $result = $apiInstance->restoreAddressbook($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->restoreAddressbook: ', $e->getMessage(), PHP_EOL;
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

## `updateAddressbook()`

```php
updateAddressbook($id, $update_addressbook_request): object
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
$update_addressbook_request = new \kruegge82\cargoInternational\Model\UpdateAddressbookRequest(); // \kruegge82\cargoInternational\Model\UpdateAddressbookRequest | Data to store

try {
    $result = $apiInstance->updateAddressbook($id, $update_addressbook_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBookApi->updateAddressbook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the record | |
| **update_addressbook_request** | [**\kruegge82\cargoInternational\Model\UpdateAddressbookRequest**](../Model/UpdateAddressbookRequest.md)| Data to store | |

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
