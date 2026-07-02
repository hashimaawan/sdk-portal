# List Notebook Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0ZSUyRiUyRkxpc3ROb3RlYm9va01ldGFkYXRh

Displays the notebook files for the specified workgroup in paginated format.

```java
CompletableFuture<ApiResponse<ListNotebookMetadataOutput>> listNotebookMetadataAsync(
    final XAmzTarget38 xAmzTarget,
    final ListNotebookMetadataInput body,
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
| `xAmzTarget` | [`XAmzTarget38`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/x-amz-target-38.md) | Header, Required | - |
| `body` | [`ListNotebookMetadataInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/list-notebook-metadata-input.md) | Body, Required | - |
| `xAmzContentSha256` | `String` | Header, Optional | - |
| `xAmzDate` | `String` | Header, Optional | - |
| `xAmzAlgorithm` | `String` | Header, Optional | - |
| `xAmzCredential` | `String` | Header, Optional | - |
| `xAmzSecurityToken` | `String` | Header, Optional | - |
| `xAmzSignature` | `String` | Header, Optional | - |
| `xAmzSignedHeaders` | `String` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ListNotebookMetadataOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/list-notebook-metadata-output.md).


# Example Usage

```java
XAmzTarget38 xAmzTarget = XAmzTarget38.ENUM_AMAZONATHENALISTNOTEBOOKMETADATA;
ListNotebookMetadataInput body = new ListNotebookMetadataInput.Builder(
    "WorkGroup8"
)
.build();


api.listNotebookMetadataAsync(xAmzTarget, body, null, null, null, null, null, null, null).thenAccept(result -> {
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
| 482 | TooManyRequestsException | `ApiException` |



