# Update Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0ZSUyRkl0ZW1zJTJGVXBkYXRlVmF1bHRJdGVt

```go
UpdateVaultItem(
    ctx context.Context,
    vaultUuid string,
    itemUuid string,
    body *models.FullItem) (
    models.ApiResponse[models.FullItem],
    error)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `string` | Template, Required | The UUID of the Item's Vault<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `itemUuid` | `string` | Template, Required | The UUID of the Item to update<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `body` | [`*models.FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/full-item.md) | Body, Optional | - |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.FullItem](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/full-item.md).


# Example Usage

```go
ctx := context.Background()

vaultUuid := "vaultUuid2"

itemUuid := "itemUuid6"

body := models.FullItem{
    Category:              models.Category_Membership,
    Favorite:              models.ToPointer(false),
    Urls:                  []models.Url{
        models.Url{
            Href:                  "https://example.com",
            Primary:               models.ToPointer(true),
        },
        models.Url{
            Href:                  "https://example.org",
        },
    },
    Vault:                 models.Vault1{
        Id:                    "id6",
    },
}

apiResponse, err := itemsApi.UpdateVaultItem(ctx, vaultUuid, itemUuid, &body)
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
| 400 | Unable to create item due to invalid input | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |



