# Get Vaults

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0ZSUyRlZhdWx0cyUyRkdldFZhdWx0cw

```go
GetVaults(
    ctx context.Context,
    filter *string) (
    models.ApiResponse[[]models.Vault],
    error)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filter` | `*string` | Query, Optional | Filter the Vault collection based on Vault name using SCIM eq filter |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [[]models.Vault](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/vault.md).


# Example Usage

```go
ctx := context.Background()

filter := "name eq \"Some Vault Name\""

apiResponse, err := vaultsApi.GetVaults(ctx, &filter)
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



