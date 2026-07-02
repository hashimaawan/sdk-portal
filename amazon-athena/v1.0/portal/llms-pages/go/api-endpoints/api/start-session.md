# Start Session

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0ZSUyRiUyRlN0YXJ0U2Vzc2lvbg

Creates a session for running calculations within a workgroup. The session is ready when it reaches an <code>IDLE</code> state.

```go
StartSession(
    ctx context.Context,
    xAmzTarget models.XAmzTarget48,
    body models.StartSessionRequest,
    xAmzContentSha256 *string,
    xAmzDate *string,
    xAmzAlgorithm *string,
    xAmzCredential *string,
    xAmzSecurityToken *string,
    xAmzSignature *string,
    xAmzSignedHeaders *string) (
    models.ApiResponse[models.StartSessionResponse],
    error)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`models.XAmzTarget48`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/x-amz-target-48.md) | Header, Required | - |
| `body` | [`models.StartSessionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/start-session-request.md) | Body, Required | - |
| `xAmzContentSha256` | `*string` | Header, Optional | - |
| `xAmzDate` | `*string` | Header, Optional | - |
| `xAmzAlgorithm` | `*string` | Header, Optional | - |
| `xAmzCredential` | `*string` | Header, Optional | - |
| `xAmzSecurityToken` | `*string` | Header, Optional | - |
| `xAmzSignature` | `*string` | Header, Optional | - |
| `xAmzSignedHeaders` | `*string` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.StartSessionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/start-session-response.md).


# Example Usage

```go
ctx := context.Background()

xAmzTarget := models.XAmzTarget48_EnumAmazonathenastartsession

body := models.StartSessionRequest{
    WorkGroup:                   "WorkGroup8",
    EngineConfiguration:         models.EngineConfiguration1{
        MaxConcurrentDpus:      94,
    },
}

apiResponse, err := api.StartSession(ctx, xAmzTarget, body, nil, nil, nil, nil, nil, nil, nil)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiError` |
| 481 | InvalidRequestException | `ApiError` |
| 482 | ResourceNotFoundException | `ApiError` |
| 483 | SessionAlreadyExistsException | `ApiError` |
| 484 | TooManyRequestsException | `ApiError` |



