# Delete Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0ZSUyRkl0ZW1zJTJGRGVsZXRlVmF1bHRJdGVt

```go
DeleteVaultItem(
    ctx context.Context,
    vaultUuid string,
    itemUuid string) (
    http.Response,
    error)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `string` | Template, Required | The UUID of the Vault the item is in<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `itemUuid` | `string` | Template, Required | The UUID of the Item to update<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |


# Response Type

**204**: Successfully deleted an item

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

vaultUuid := "vaultUuid2"

itemUuid := "itemUuid6"

resp, err := itemsApi.DeleteVaultItem(ctx, vaultUuid, itemUuid)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.ErrorResponse:
            log.Fatalln("ErrorResponseException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    fmt.Println(resp.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |



