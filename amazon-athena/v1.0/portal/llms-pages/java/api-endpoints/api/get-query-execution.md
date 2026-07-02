# Get Query Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0ZSUyRiUyRkdldFF1ZXJ5RXhlY3V0aW9u

Returns information about a single execution of a query if you have access to the workgroup in which the query ran. Each time a query executes, information about the query execution is saved with a unique ID.

```java
CompletableFuture<ApiResponse<GetQueryExecutionOutput>> getQueryExecutionAsync(
    final XAmzTarget23 xAmzTarget,
    final GetQueryExecutionInput body,
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
| `xAmzTarget` | [`XAmzTarget23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/x-amz-target-23.md) | Header, Required | - |
| `body` | [`GetQueryExecutionInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/get-query-execution-input.md) | Body, Required | - |
| `xAmzContentSha256` | `String` | Header, Optional | - |
| `xAmzDate` | `String` | Header, Optional | - |
| `xAmzAlgorithm` | `String` | Header, Optional | - |
| `xAmzCredential` | `String` | Header, Optional | - |
| `xAmzSecurityToken` | `String` | Header, Optional | - |
| `xAmzSignature` | `String` | Header, Optional | - |
| `xAmzSignedHeaders` | `String` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`GetQueryExecutionOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/get-query-execution-output.md).


# Example Usage

```java
XAmzTarget23 xAmzTarget = XAmzTarget23.ENUM_AMAZONATHENAGETQUERYEXECUTION;
GetQueryExecutionInput body = new GetQueryExecutionInput.Builder(
    "QueryExecutionId0"
)
.build();


api.getQueryExecutionAsync(xAmzTarget, body, null, null, null, null, null, null, null).thenAccept(result -> {
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



