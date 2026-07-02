# Update Data Catalog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0ZSUyRiUyRlVwZGF0ZURhdGFDYXRhbG9n

Updates the data catalog that has the specified name.

```php
function updateDataCatalog(
    string $xAmzTarget,
    UpdateDataCatalogInput $body,
    ?string $xAmzContentSha256 = null,
    ?string $xAmzDate = null,
    ?string $xAmzAlgorithm = null,
    ?string $xAmzCredential = null,
    ?string $xAmzSecurityToken = null,
    ?string $xAmzSignature = null,
    ?string $xAmzSignedHeaders = null
): array
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`string(XAmzTarget54Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/x-amz-target-54.md) | Header, Required | - |
| `body` | [`UpdateDataCatalogInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/update-data-catalog-input.md) | Body, Required | - |
| `xAmzContentSha256` | `?string` | Header, Optional | - |
| `xAmzDate` | `?string` | Header, Optional | - |
| `xAmzAlgorithm` | `?string` | Header, Optional | - |
| `xAmzCredential` | `?string` | Header, Optional | - |
| `xAmzSecurityToken` | `?string` | Header, Optional | - |
| `xAmzSignature` | `?string` | Header, Optional | - |
| `xAmzSignedHeaders` | `?string` | Header, Optional | - |


# Response Type

**200**: Success

`array`


# Example Usage

```php
$xAmzTarget = XAmzTarget54Enum::ENUM_AMAZONATHENAUPDATEDATACATALOG;

$body = UpdateDataCatalogInputBuilder::init(
    'Name6',
    DataCatalogType3Enum::HIVE
)->build();

$aPIController = $client->getAPIController();

try {
    $result = $aPIController->updateDataCatalog(
        $xAmzTarget,
        $body
    );
    echo 'array:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiException` |
| 481 | InvalidRequestException | `ApiException` |



