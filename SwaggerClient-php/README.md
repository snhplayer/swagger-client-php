# SwaggerClient-php
API для создания, чтения, обновления и удаления элементов.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/git_user_id/git_repo_id.git"
    }
  ],
  "require": {
    "git_user_id/git_repo_id": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *http://localhost/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**itemsAddPost**](docs/Api/DefaultApi.md#itemsaddpost) | **POST** /items_add | Добавление нового элемента
*DefaultApi* | [**itemsDeleteIdDelete**](docs/Api/DefaultApi.md#itemsdeleteiddelete) | **DELETE** /items_delete/{id} | Удаление элемента
*DefaultApi* | [**itemsGet**](docs/Api/DefaultApi.md#itemsget) | **GET** /items | Получение списка элементов
*DefaultApi* | [**itemsUpdateIdPut**](docs/Api/DefaultApi.md#itemsupdateidput) | **PUT** /items_update/{id} | Обновление элемента

## Documentation For Models

 - [InlineResponse200](docs/Model/InlineResponse200.md)
 - [ItemsAddBody](docs/Model/ItemsAddBody.md)
 - [ItemsUpdateIdBody](docs/Model/ItemsUpdateIdBody.md)

## Documentation For Authorization

 All endpoints do not require authorization.


## Author



