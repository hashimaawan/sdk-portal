# Terminate Session

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0ZSUyRiUyRlRlcm1pbmF0ZVNlc3Npb24

Terminates an active session. A <code>TerminateSession</code> call on a session that is already inactive (for example, in a <code>FAILED</code>, <code>TERMINATED</code> or <code>TERMINATING</code> state) succeeds but has no effect. Calculations running in the session when <code>TerminateSession</code> is called are forcefully stopped, but may display as <code>FAILED</code> instead of <code>STOPPED</code>.

```go
TerminateSession(
    ctx context.Context,
    xAmzTarget models.XAmzTarget52,
    body models.TerminateSessionRequest,
    xAmzContentSha256 *string,
    xAmzDate *string,
    xAmzAlgorithm *string,
    xAmzCredential *string,
    xAmzSecurityToken *string,
    xAmzSignature *string,
    xAmzSignedHeaders *string) (
    models.ApiResponse[models.TerminateSessionResponse],
    error)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`models.XAmzTarget52`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/x-amz-target-52.md) | Header, Required | - |
| `body` | [`models.TerminateSessionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/terminate-session-request.md) | Body, Required | - |
| `xAmzContentSha256` | `*string` | Header, Optional | - |
| `xAmzDate` | `*string` | Header, Optional | - |
| `xAmzAlgorithm` | `*string` | Header, Optional | - |
| `xAmzCredential` | `*string` | Header, Optional | - |
| `xAmzSecurityToken` | `*string` | Header, Optional | - |
| `xAmzSignature` | `*string` | Header, Optional | - |
| `xAmzSignedHeaders` | `*string` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.TerminateSessionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/terminate-session-response.md).


# Example Usage

```go
ctx := context.Background()

xAmzTarget := models.XAmzTarget52_EnumAmazonathenaterminatesession

body := models.TerminateSessionRequest{
    SessionId:             "SessionId2",
}

apiResponse, err := api.TerminateSession(ctx, xAmzTarget, body, nil, nil, nil, nil, nil, nil, nil)
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



