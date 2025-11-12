# kruegge82\cargoInternational\CarrierTemplatesApi



All URIs are relative to https://app.spedition.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listCarrierTemplates()**](CarrierTemplatesApi.md#listCarrierTemplates) | **GET** /api/templates/carrier/index | List records with pagination |


## `listCarrierTemplates()`

```php
listCarrierTemplates($per_page, $page): \kruegge82\cargoInternational\Model\PaginatedResponse
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


$apiInstance = new kruegge82\cargoInternational\Api\CarrierTemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records per page
$page = 56; // int | The starting page for pagination

try {
    $result = $apiInstance->listCarrierTemplates($per_page, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarrierTemplatesApi->listCarrierTemplates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records per page | [optional] |
| **page** | **int**| The starting page for pagination | [optional] |

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
