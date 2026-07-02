# List Data Catalogs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0ZSUyRiUyRkxpc3REYXRhQ2F0YWxvZ3M

<p>Lists the data catalogs in the current Amazon Web Services account.</p> <note> <p>In the Athena console, data catalogs are listed as "data sources" on the <b>Data sources</b> page under the <b>Data source name</b> column.</p> </note>


```go
ListDataCatalogs(
    ctx context.Context,
    xAmzTarget models.XAmzTarget33,
    body models.ListDataCatalogsInput,
    xAmzContentSha256 *string,
    xAmzDate *string,
    xAmzAlgorithm *string,
    xAmzCredential *string,
    xAmzSecurityToken *string,
    xAmzSignature *string,
    xAmzSignedHeaders *string,
    maxResults *string,
    nextToken *string) (
    models.ApiResponse[models.ListDataCatalogsOutput],
    error)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`models.XAmzTarget33`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/x-amz-target-33.md) | Header, Required | - |
| `body` | [`models.ListDataCatalogsInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/list-data-catalogs-input.md) | Body, Required | - |
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ListDataCatalogsOutput](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/list-data-catalogs-output.md).


# Example Usage

```go
ctx := context.Background()

xAmzTarget := models.XAmzTarget33_EnumAmazonathenalistdatacatalogs

body := models.ListDataCatalogsInput{
}

apiResponse, err := api.ListDataCatalogs(ctx, xAmzTarget, body, nil, nil, nil, nil, nil, nil, nil, nil, nil)
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



