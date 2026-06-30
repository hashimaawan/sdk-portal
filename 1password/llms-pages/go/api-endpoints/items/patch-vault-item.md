# Patch Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0ZSUyRkl0ZW1zJTJGUGF0Y2hWYXVsdEl0ZW0

Applies a modified [RFC6902 JSON Patch](https://tools.ietf.org/html/rfc6902) document to an Item or ItemField. This endpoint only supports `add`, `remove` and `replace` operations.

When modifying a specific ItemField, the ItemField's ID in the `path` attribute of the operation object: `/fields/{fieldId}`

```go
PatchVaultItem(
    ctx context.Context,
    vaultUuid string,
    itemUuid string,
    body []models.Patch) (
    models.ApiResponse[models.FullItem],
    error)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `string` | Template, Required | The UUID of the Vault the item is in<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `itemUuid` | `string` | Template, Required | The UUID of the Item to update<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `body` | [`[]models.Patch`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/patch.md) | Body, Optional | - |


# Response Type

**200**: OK - Item updated. If no Patch operations were provided, Item is unmodified.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.FullItem](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/full-item.md).


# Example Usage

```go
ctx := context.Background()

vaultUuid := "vaultUuid2"

itemUuid := "itemUuid6"

body := []models.Patch{
    models.Patch{
        Op:                    models.Op_Add,
        Path:                  "/fields",
        Value:                 models.ToPointer(interface{}("[label, New Field][type, string][value, hunter2]")),
    },
}

apiResponse, err := itemsApi.PatchVaultItem(ctx, vaultUuid, itemUuid, body)
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
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |



