# List Prepared Statements

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0ZSUyRiUyRkxpc3RQcmVwYXJlZFN0YXRlbWVudHM

Lists the prepared statements in the specified workgroup.

```php
function listPreparedStatements(
    string $xAmzTarget,
    ListPreparedStatementsInput $body,
    ?string $xAmzContentSha256 = null,
    ?string $xAmzDate = null,
    ?string $xAmzAlgorithm = null,
    ?string $xAmzCredential = null,
    ?string $xAmzSecurityToken = null,
    ?string $xAmzSignature = null,
    ?string $xAmzSignedHeaders = null,
    ?string $maxResults = null,
    ?string $nextToken = null
): ListPreparedStatementsOutput
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`string(XAmzTarget40Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/x-amz-target-40.md) | Header, Required | - |
| `body` | [`ListPreparedStatementsInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/list-prepared-statements-input.md) | Body, Required | - |
| `xAmzContentSha256` | `?string` | Header, Optional | - |
| `xAmzDate` | `?string` | Header, Optional | - |
| `xAmzAlgorithm` | `?string` | Header, Optional | - |
| `xAmzCredential` | `?string` | Header, Optional | - |
| `xAmzSecurityToken` | `?string` | Header, Optional | - |
| `xAmzSignature` | `?string` | Header, Optional | - |
| `xAmzSignedHeaders` | `?string` | Header, Optional | - |
| `maxResults` | `?string` | Query, Optional | Pagination limit |
| `nextToken` | `?string` | Query, Optional | Pagination token |


# Response Type

**200**: Success

[`ListPreparedStatementsOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/list-prepared-statements-output.md)


# Example Usage

```php
$xAmzTarget = XAmzTarget40Enum::ENUM_AMAZONATHENALISTPREPAREDSTATEMENTS;

$body = ListPreparedStatementsInputBuilder::init(
    'WorkGroup8'
)->build();

$aPIController = $client->getAPIController();

try {
    $result = $aPIController->listPreparedStatements(
        $xAmzTarget,
        $body
    );
    echo 'ListPreparedStatementsOutput:';
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



