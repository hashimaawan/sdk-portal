# Batch Get Prepared Statement

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0ZSUyRiUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnQ

Returns the details of a single prepared statement or a list of up to 256 prepared statements for the array of prepared statement names that you provide. Requires you to have access to the workgroup to which the prepared statements belong. If a prepared statement cannot be retrieved for the name specified, the statement is listed in <code>UnprocessedPreparedStatementNames</code>.

```php
function batchGetPreparedStatement(
    string $xAmzTarget,
    BatchGetPreparedStatementInput $body,
    ?string $xAmzContentSha256 = null,
    ?string $xAmzDate = null,
    ?string $xAmzAlgorithm = null,
    ?string $xAmzCredential = null,
    ?string $xAmzSecurityToken = null,
    ?string $xAmzSignature = null,
    ?string $xAmzSignedHeaders = null
): ApiResponse
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`string(XAmzTarget1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/x-amz-target-1.md) | Header, Required | - |
| `body` | [`BatchGetPreparedStatementInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/batch-get-prepared-statement-input.md) | Body, Required | - |
| `xAmzContentSha256` | `?string` | Header, Optional | - |
| `xAmzDate` | `?string` | Header, Optional | - |
| `xAmzAlgorithm` | `?string` | Header, Optional | - |
| `xAmzCredential` | `?string` | Header, Optional | - |
| `xAmzSecurityToken` | `?string` | Header, Optional | - |
| `xAmzSignature` | `?string` | Header, Optional | - |
| `xAmzSignedHeaders` | `?string` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`BatchGetPreparedStatementOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/batch-get-prepared-statement-output.md).


# Example Usage

```php
$xAmzTarget = XAmzTarget1::ENUM_AMAZONATHENABATCHGETPREPAREDSTATEMENT;

$body = BatchGetPreparedStatementInputBuilder::init(
    [
        'PreparedStatementNames0',
        'PreparedStatementNames1',
        'PreparedStatementNames2'
    ],
    'WorkGroup8'
)->build();

$api = $client->getAPI();
$apiResponse = $api->batchGetPreparedStatement(
    $xAmzTarget,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'BatchGetPreparedStatementOutput:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiException` |
| 481 | InvalidRequestException | `ApiException` |



