# Start Session

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlN0YXJ0U2Vzc2lvbg

Creates a session for running calculations within a workgroup. The session is ready when it reaches an <code>IDLE</code> state.

```csharp
StartSessionAsync(
    Models.XAmzTarget48 xAmzTarget,
    Models.StartSessionRequest body,
    string xAmzContentSha256 = null,
    string xAmzDate = null,
    string xAmzAlgorithm = null,
    string xAmzCredential = null,
    string xAmzSecurityToken = null,
    string xAmzSignature = null,
    string xAmzSignedHeaders = null)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`XAmzTarget48`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/x-amz-target-48.md) | Header, Required | - |
| `body` | [`StartSessionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/start-session-request.md) | Body, Required | - |
| `xAmzContentSha256` | `string` | Header, Optional | - |
| `xAmzDate` | `string` | Header, Optional | - |
| `xAmzAlgorithm` | `string` | Header, Optional | - |
| `xAmzCredential` | `string` | Header, Optional | - |
| `xAmzSecurityToken` | `string` | Header, Optional | - |
| `xAmzSignature` | `string` | Header, Optional | - |
| `xAmzSignedHeaders` | `string` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.StartSessionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/start-session-response.md).


# Example Usage

```csharp
XAmzTarget48 xAmzTarget = XAmzTarget48.EnumAmazonAthenaStartSession;
StartSessionRequest body = new StartSessionRequest
{
    WorkGroup = "WorkGroup8",
    EngineConfiguration = new EngineConfiguration1
    {
        MaxConcurrentDpus = 94,
    },
};

try
{
    ApiResponse<StartSessionResponse> result = await api.StartSessionAsync(
        xAmzTarget,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiException` |
| 481 | InvalidRequestException | `ApiException` |
| 482 | ResourceNotFoundException | `ApiException` |
| 483 | SessionAlreadyExistsException | `ApiException` |
| 484 | TooManyRequestsException | `ApiException` |



