# Batch Get Prepared Statement

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0ZSUyRiUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnQ

Returns the details of a single prepared statement or a list of up to 256 prepared statements for the array of prepared statement names that you provide. Requires you to have access to the workgroup to which the prepared statements belong. If a prepared statement cannot be retrieved for the name specified, the statement is listed in <code>UnprocessedPreparedStatementNames</code>.

```java
CompletableFuture<ApiResponse<BatchGetPreparedStatementOutput>> batchGetPreparedStatementAsync(
    final XAmzTarget1 xAmzTarget,
    final BatchGetPreparedStatementInput body,
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
| `xAmzTarget` | [`XAmzTarget1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/x-amz-target-1.md) | Header, Required | - |
| `body` | [`BatchGetPreparedStatementInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/batch-get-prepared-statement-input.md) | Body, Required | - |
| `xAmzContentSha256` | `String` | Header, Optional | - |
| `xAmzDate` | `String` | Header, Optional | - |
| `xAmzAlgorithm` | `String` | Header, Optional | - |
| `xAmzCredential` | `String` | Header, Optional | - |
| `xAmzSecurityToken` | `String` | Header, Optional | - |
| `xAmzSignature` | `String` | Header, Optional | - |
| `xAmzSignedHeaders` | `String` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`BatchGetPreparedStatementOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/batch-get-prepared-statement-output.md).


# Example Usage

```java
XAmzTarget1 xAmzTarget = XAmzTarget1.ENUM_AMAZONATHENABATCHGETPREPAREDSTATEMENT;
BatchGetPreparedStatementInput body = new BatchGetPreparedStatementInput.Builder(
    Arrays.asList(
        "PreparedStatementNames0",
        "PreparedStatementNames1",
        "PreparedStatementNames2"
    ),
    "WorkGroup8"
)
.build();


api.batchGetPreparedStatementAsync(xAmzTarget, body, null, null, null, null, null, null, null).thenAccept(result -> {
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



