# Get Calculation Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0ZSUyRiUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9u

Describes a previously submitted calculation execution.

```java
CompletableFuture<ApiResponse<GetCalculationExecutionResponse>> getCalculationExecutionAsync(
    final XAmzTarget15 xAmzTarget,
    final GetCalculationExecutionRequest body,
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
| `xAmzTarget` | [`XAmzTarget15`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/x-amz-target-15.md) | Header, Required | - |
| `body` | [`GetCalculationExecutionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/get-calculation-execution-request.md) | Body, Required | - |
| `xAmzContentSha256` | `String` | Header, Optional | - |
| `xAmzDate` | `String` | Header, Optional | - |
| `xAmzAlgorithm` | `String` | Header, Optional | - |
| `xAmzCredential` | `String` | Header, Optional | - |
| `xAmzSecurityToken` | `String` | Header, Optional | - |
| `xAmzSignature` | `String` | Header, Optional | - |
| `xAmzSignedHeaders` | `String` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`GetCalculationExecutionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/get-calculation-execution-response.md).


# Example Usage

```java
XAmzTarget15 xAmzTarget = XAmzTarget15.ENUM_AMAZONATHENAGETCALCULATIONEXECUTION;
GetCalculationExecutionRequest body = new GetCalculationExecutionRequest.Builder(
    "CalculationExecutionId8"
)
.build();


api.getCalculationExecutionAsync(xAmzTarget, body, null, null, null, null, null, null, null).thenAccept(result -> {
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



