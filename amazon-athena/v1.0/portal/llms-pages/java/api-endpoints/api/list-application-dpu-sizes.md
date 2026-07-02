# List Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0ZSUyRiUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVz

Returns the supported DPU sizes for the supported application runtimes (for example, <code>Athena notebook version 1</code>).

```java
CompletableFuture<ListApplicationDPUSizesOutput> listApplicationDPUSizesAsync(
    final XAmzTarget31Enum xAmzTarget,
    final ListApplicationDPUSizesInput body,
    final String xAmzContentSha256,
    final String xAmzDate,
    final String xAmzAlgorithm,
    final String xAmzCredential,
    final String xAmzSecurityToken,
    final String xAmzSignature,
    final String xAmzSignedHeaders,
    final String maxResults,
    final String nextToken)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`XAmzTarget31Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/x-amz-target-31.md) | Header, Required | - |
| `body` | [`ListApplicationDPUSizesInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/list-application-dpu-sizes-input.md) | Body, Required | - |
| `xAmzContentSha256` | `String` | Header, Optional | - |
| `xAmzDate` | `String` | Header, Optional | - |
| `xAmzAlgorithm` | `String` | Header, Optional | - |
| `xAmzCredential` | `String` | Header, Optional | - |
| `xAmzSecurityToken` | `String` | Header, Optional | - |
| `xAmzSignature` | `String` | Header, Optional | - |
| `xAmzSignedHeaders` | `String` | Header, Optional | - |
| `maxResults` | `String` | Query, Optional | Pagination limit |
| `nextToken` | `String` | Query, Optional | Pagination token |


# Response Type

**200**: Success

[`ListApplicationDPUSizesOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/list-application-dpu-sizes-output.md)


# Example Usage

```java
XAmzTarget31Enum xAmzTarget = XAmzTarget31Enum.ENUM_AMAZONATHENALISTAPPLICATIONDPUSIZES;
ListApplicationDPUSizesInput body = new ListApplicationDPUSizesInput.Builder()
    .build();


aPIController.listApplicationDPUSizesAsync(xAmzTarget, body, null, null, null, null, null, null, null, null, null).thenAccept(result -> {
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



