# List Calculation Executions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0ZSUyRiUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnM

Lists the calculations that have been submitted to a session in descending order. Newer calculations are listed first; older calculations are listed later.

```java
CompletableFuture<ApiResponse<ListCalculationExecutionsResponse>> listCalculationExecutionsAsync(
    final XAmzTarget32 xAmzTarget,
    final ListCalculationExecutionsRequest body,
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
| `xAmzTarget` | [`XAmzTarget32`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/x-amz-target-32.md) | Header, Required | - |
| `body` | [`ListCalculationExecutionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/list-calculation-executions-request.md) | Body, Required | - |
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ListCalculationExecutionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/list-calculation-executions-response.md).


# Example Usage

```java
XAmzTarget32 xAmzTarget = XAmzTarget32.ENUM_AMAZONATHENALISTCALCULATIONEXECUTIONS;
ListCalculationExecutionsRequest body = new ListCalculationExecutionsRequest.Builder(
    "SessionId2"
)
.build();


api.listCalculationExecutionsAsync(xAmzTarget, body, null, null, null, null, null, null, null, null, null).thenAccept(result -> {
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



