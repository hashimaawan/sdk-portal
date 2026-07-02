# List Executors

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0ZSUyRiUyRkxpc3RFeGVjdXRvcnM

Lists, in descending order, the executors that joined a session. Newer executors are listed first; older executors are listed later. The result can be optionally filtered by state.

```go
ListExecutors(
    ctx context.Context,
    xAmzTarget models.XAmzTarget36,
    body models.ListExecutorsRequest,
    xAmzContentSha256 *string,
    xAmzDate *string,
    xAmzAlgorithm *string,
    xAmzCredential *string,
    xAmzSecurityToken *string,
    xAmzSignature *string,
    xAmzSignedHeaders *string,
    maxResults *string,
    nextToken *string) (
    models.ApiResponse[models.ListExecutorsResponse],
    error)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`models.XAmzTarget36`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/x-amz-target-36.md) | Header, Required | - |
| `body` | [`models.ListExecutorsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/list-executors-request.md) | Body, Required | - |
| `xAmzContentSha256` | `*string` | Header, Optional | - |
| `xAmzDate` | `*string` | Header, Optional | - |
| `xAmzAlgorithm` | `*string` | Header, Optional | - |
| `xAmzCredential` | `*string` | Header, Optional | - |
| `xAmzSecurityToken` | `*string` | Header, Optional | - |
| `xAmzSignature` | `*string` | Header, Optional | - |
| `xAmzSignedHeaders` | `*string` | Header, Optional | - |
| `maxResults` | `*string` | Query, Optional | Pagination limit |
| `nextToken` | `*string` | Query, Optional | Pagination token |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ListExecutorsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/list-executors-response.md).


# Example Usage

```go
ctx := context.Background()

xAmzTarget := models.XAmzTarget36_EnumAmazonathenalistexecutors

body := models.ListExecutorsRequest{
    SessionId:             "SessionId2",
}

apiResponse, err := api.ListExecutors(ctx, xAmzTarget, body, nil, nil, nil, nil, nil, nil, nil, nil, nil)
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



