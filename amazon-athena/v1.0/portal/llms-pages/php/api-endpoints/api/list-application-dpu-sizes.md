# List Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0ZSUyRiUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVz

Returns the supported DPU sizes for the supported application runtimes (for example, <code>Athena notebook version 1</code>).

```php
function listApplicationDPUSizes(
    string $xAmzTarget,
    ListApplicationDPUSizesInput $body,
    ?string $xAmzContentSha256 = null,
    ?string $xAmzDate = null,
    ?string $xAmzAlgorithm = null,
    ?string $xAmzCredential = null,
    ?string $xAmzSecurityToken = null,
    ?string $xAmzSignature = null,
    ?string $xAmzSignedHeaders = null,
    ?string $maxResults = null,
    ?string $nextToken = null
): ListApplicationDPUSizesOutput
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`string(XAmzTarget31Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/x-amz-target-31.md) | Header, Required | - |
| `body` | [`ListApplicationDPUSizesInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/list-application-dpu-sizes-input.md) | Body, Required | - |
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

[`ListApplicationDPUSizesOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/list-application-dpu-sizes-output.md)


# Example Usage

```php
$xAmzTarget = XAmzTarget31Enum::ENUM_AMAZONATHENALISTAPPLICATIONDPUSIZES;

$body = ListApplicationDPUSizesInputBuilder::init()->build();

$aPIController = $client->getAPIController();

try {
    $result = $aPIController->listApplicationDPUSizes(
        $xAmzTarget,
        $body
    );
    echo 'ListApplicationDPUSizesOutput:';
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
| 482 | TooManyRequestsException | `ApiException` |



