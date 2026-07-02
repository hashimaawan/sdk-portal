# Create Presigned Notebook Url

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0ZSUyRiUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJs

Gets an authentication token and the URL at which the notebook can be accessed. During programmatic access, <code>CreatePresignedNotebookUrl</code> must be called every 10 minutes to refresh the authentication token. For information about granting programmatic access, see <a href="https://docs.aws.amazon.com/athena/latest/ug/setting-up.html#setting-up-grant-programmatic-access">Grant programmatic access</a>.

```java
CompletableFuture<ApiResponse<CreatePresignedNotebookUrlResponse>> createPresignedNotebookUrlAsync(
    final XAmzTarget7 xAmzTarget,
    final CreatePresignedNotebookUrlRequest body,
    final String xAmzContentSha256,
    final String xAmzDate,
    final String xAmzAlgorithm,
    final String xAmzCredential,
    final String xAmzSecurityToken,
    final String xAmzSignature,
    final String xAmzSignedHeaders)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`XAmzTarget7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/x-amz-target-7.md) | Header, Required | - |
| `body` | [`CreatePresignedNotebookUrlRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/create-presigned-notebook-url-request.md) | Body, Required | - |
| `xAmzContentSha256` | `String` | Header, Optional | - |
| `xAmzDate` | `String` | Header, Optional | - |
| `xAmzAlgorithm` | `String` | Header, Optional | - |
| `xAmzCredential` | `String` | Header, Optional | - |
| `xAmzSecurityToken` | `String` | Header, Optional | - |
| `xAmzSignature` | `String` | Header, Optional | - |
| `xAmzSignedHeaders` | `String` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CreatePresignedNotebookUrlResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/create-presigned-notebook-url-response.md).


# Example Usage

```java
XAmzTarget7 xAmzTarget = XAmzTarget7.ENUM_AMAZONATHENACREATEPRESIGNEDNOTEBOOKURL;
CreatePresignedNotebookUrlRequest body = new CreatePresignedNotebookUrlRequest.Builder(
    "SessionId2"
)
.build();


api.createPresignedNotebookUrlAsync(xAmzTarget, body, null, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiException` |
| 481 | InvalidRequestException | `ApiException` |
| 482 | ResourceNotFoundException | `ApiException` |



