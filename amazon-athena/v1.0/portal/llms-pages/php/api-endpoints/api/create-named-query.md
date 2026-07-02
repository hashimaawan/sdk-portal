# Create Named Query

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0ZSUyRiUyRkNyZWF0ZU5hbWVkUXVlcnk

<p>Creates a named query in the specified workgroup. Requires that you have access to the workgroup.</p> <p>For code samples using the Amazon Web Services SDK for Java, see <a href="http://docs.aws.amazon.com/athena/latest/ug/code-samples.html">Examples and Code Samples</a> in the <i>Amazon Athena User Guide</i>.</p>


```php
function createNamedQuery(
    string $xAmzTarget,
    CreateNamedQueryInput $body,
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
| `xAmzTarget` | [`string(XAmzTarget4)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/x-amz-target-4.md) | Header, Required | - |
| `body` | [`CreateNamedQueryInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/create-named-query-input.md) | Body, Required | - |
| `xAmzContentSha256` | `?string` | Header, Optional | - |
| `xAmzDate` | `?string` | Header, Optional | - |
| `xAmzAlgorithm` | `?string` | Header, Optional | - |
| `xAmzCredential` | `?string` | Header, Optional | - |
| `xAmzSecurityToken` | `?string` | Header, Optional | - |
| `xAmzSignature` | `?string` | Header, Optional | - |
| `xAmzSignedHeaders` | `?string` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`CreateNamedQueryOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/create-named-query-output.md).


# Example Usage

```php
$xAmzTarget = XAmzTarget4::ENUM_AMAZONATHENACREATENAMEDQUERY;

$body = CreateNamedQueryInputBuilder::init(
    'Name6',
    'Database4',
    'QueryString8'
)->build();

$api = $client->getAPI();
$apiResponse = $api->createNamedQuery(
    $xAmzTarget,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'CreateNamedQueryOutput:';
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



