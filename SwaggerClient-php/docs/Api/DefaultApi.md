# Swagger\Client\DefaultApi

All URIs are relative to *http://localhost/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**itemsAddPost**](DefaultApi.md#itemsaddpost) | **POST** /items_add | Добавление нового элемента
[**itemsDeleteIdDelete**](DefaultApi.md#itemsdeleteiddelete) | **DELETE** /items_delete/{id} | Удаление элемента
[**itemsGet**](DefaultApi.md#itemsget) | **GET** /items | Получение списка элементов
[**itemsUpdateIdPut**](DefaultApi.md#itemsupdateidput) | **PUT** /items_update/{id} | Обновление элемента

# **itemsAddPost**
> \Swagger\Client\Model\InlineResponse200 itemsAddPost($body)

Добавление нового элемента

Добавляет новый элемент в список.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\ItemsAddBody(); // \Swagger\Client\Model\ItemsAddBody | 

try {
    $result = $apiInstance->itemsAddPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->itemsAddPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ItemsAddBody**](../Model/ItemsAddBody.md)|  |

### Return type

[**\Swagger\Client\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **itemsDeleteIdDelete**
> itemsDeleteIdDelete($id)

Удаление элемента

Удаляет элемент по его ID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 56; // int | ID элемента для удаления

try {
    $apiInstance->itemsDeleteIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->itemsDeleteIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID элемента для удаления |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **itemsGet**
> \Swagger\Client\Model\InlineResponse200[] itemsGet($sort)

Получение списка элементов

Возвращает список всех элементов с возможностью сортировки.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$sort = "sort_example"; // string | Порядок сортировки (ASC или DESC).

try {
    $result = $apiInstance->itemsGet($sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->itemsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sort** | **string**| Порядок сортировки (ASC или DESC). | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse200[]**](../Model/InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **itemsUpdateIdPut**
> itemsUpdateIdPut($body, $id)

Обновление элемента

Обновляет значение элемента по его ID.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\ItemsUpdateIdBody(); // \Swagger\Client\Model\ItemsUpdateIdBody | 
$id = 56; // int | ID элемента для обновления

try {
    $apiInstance->itemsUpdateIdPut($body, $id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->itemsUpdateIdPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ItemsUpdateIdBody**](../Model/ItemsUpdateIdBody.md)|  |
 **id** | **int**| ID элемента для обновления |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

