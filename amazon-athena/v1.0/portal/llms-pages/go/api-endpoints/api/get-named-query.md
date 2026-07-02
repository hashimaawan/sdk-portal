# Get Named Query

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0ZSUyRiUyRkdldE5hbWVkUXVlcnk

Returns information about a single query. Requires that you have access to the workgroup in which the query was saved.

```go
GetNamedQuery(
    ctx context.Context,
    xAmzTarget models.XAmzTarget20,
    body models.GetNamedQueryInput,
    xAmzContentSha256 *string,
    xAmzDate *string,
    xAmzAlgorithm *string,
    xAmzCredential *string,
    xAmzSecurityToken *string,
    xAmzSignature *string,
    xAmzSignedHeaders *string) (
    models.ApiResponse[models.GetNamedQueryOutput],
    error)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`models.XAmzTarget20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/x-amz-target-20.md) | Header, Required | - |
| `body` | [`models.GetNamedQueryInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/get-named-query-input.md) | Body, Required | - |
| `xAmzContentSha256` | `*string` | Header, Optional | - |
| `xAmzDate` | `*string` | Header, Optional | - |
| `xAmzAlgorithm` | `*string` | Header, Optional | - |
| `xAmzCredential` | `*string` | Header, Optional | - |
| `xAmzSecurityToken` | `*string` | Header, Optional | - |
| `xAmzSignature` | `*string` | Header, Optional | - |
| `xAmzSignedHeaders` | `*string` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.GetNamedQueryOutput](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/get-named-query-output.md).


# Example Usage

```go
ctx := context.Background()

xAmzTarget := models.XAmzTarget20_EnumAmazonathenagetnamedquery

body := models.GetNamedQueryInput{
    NamedQueryId:          "NamedQueryId6",
}

apiResponse, err := api.GetNamedQuery(ctx, xAmzTarget, body, nil, nil, nil, nil, nil, nil, nil)
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



