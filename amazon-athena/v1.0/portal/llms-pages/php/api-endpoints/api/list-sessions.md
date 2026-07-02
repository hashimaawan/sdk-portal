# List Sessions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0ZSUyRiUyRkxpc3RTZXNzaW9ucw

Lists the sessions in a workgroup that are in an active state like <code>CREATING</code>, <code>CREATED</code>, <code>IDLE</code>, or <code>BUSY</code>. Newer sessions are listed first; older sessions are listed later.

```php
function listSessions(
    string $xAmzTarget,
    ListSessionsRequest $body,
    ?string $xAmzContentSha256 = null,
    ?string $xAmzDate = null,
    ?string $xAmzAlgorithm = null,
    ?string $xAmzCredential = null,
    ?string $xAmzSecurityToken = null,
    ?string $xAmzSignature = null,
    ?string $xAmzSignedHeaders = null,
    ?string $maxResults = null,
    ?string $nextToken = null
): ApiResponse
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`string(XAmzTarget42)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/x-amz-target-42.md) | Header, Required | - |
| `body` | [`ListSessionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/list-sessions-request.md) | Body, Required | - |
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListSessionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/list-sessions-response.md).


# Example Usage

```php
$xAmzTarget = XAmzTarget42::ENUM_AMAZONATHENALISTSESSIONS;

$body = ListSessionsRequestBuilder::init(
    'WorkGroup8'
)->build();

$api = $client->getAPI();
$apiResponse = $api->listSessions(
    $xAmzTarget,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListSessionsResponse:';
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
| 482 | ResourceNotFoundException | `ApiException` |



