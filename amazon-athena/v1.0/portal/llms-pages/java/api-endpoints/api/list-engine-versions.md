# List Engine Versions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0ZSUyRiUyRkxpc3RFbmdpbmVWZXJzaW9ucw

Returns a list of engine versions that are available to choose from, including the Auto option.

```java
CompletableFuture<ListEngineVersionsOutput> listEngineVersionsAsync(
    final XAmzTarget35Enum xAmzTarget,
    final ListEngineVersionsInput body,
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
| `xAmzTarget` | [`XAmzTarget35Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/x-amz-target-35.md) | Header, Required | - |
| `body` | [`ListEngineVersionsInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/list-engine-versions-input.md) | Body, Required | - |
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

[`ListEngineVersionsOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/list-engine-versions-output.md)


# Example Usage

```java
XAmzTarget35Enum xAmzTarget = XAmzTarget35Enum.ENUM_AMAZONATHENALISTENGINEVERSIONS;
ListEngineVersionsInput body = new ListEngineVersionsInput.Builder()
    .build();


aPIController.listEngineVersionsAsync(xAmzTarget, body, null, null, null, null, null, null, null, null, null).thenAccept(result -> {
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



