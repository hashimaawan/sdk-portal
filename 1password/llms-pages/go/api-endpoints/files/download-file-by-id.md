# Download File by ID

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0ZSUyRkZpbGVzJTJGRG93bmxvYWRGaWxlQnlJRA

```go
DownloadFileById(
    ctx context.Context,
    vaultUuid uuid.UUID,
    itemUuid uuid.UUID,
    fileUuid string) (
    models.ApiResponse[[]byte],
    error)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `uuid.UUID` | Template, Required | The UUID of the Vault the item is in |
| `itemUuid` | `uuid.UUID` | Template, Required | The UUID of the Item the File is in |
| `fileUuid` | `string` | Template, Required | UUID of the file to get content from |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type []byte.


# Example Usage

```go
ctx := context.Background()

vaultUuid := uuid.MustParse("00002186-0000-0000-0000-000000000000")

itemUuid := uuid.MustParse("0000141a-0000-0000-0000-000000000000")

fileUuid := "fileUuid2"

apiResponse, err := filesApi.DownloadFileById(ctx, vaultUuid, itemUuid, fileUuid)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.ErrorResponse:
            log.Fatalln("ErrorResponseException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |
| 404 | File not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |



