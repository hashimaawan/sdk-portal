# Get Vaults

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0ZSUyRlZhdWx0cyUyRkdldFZhdWx0cw

```csharp
GetVaultsAsync(
    string filter = null)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filter` | `string` | Query, Optional | Filter the Vault collection based on Vault name using SCIM eq filter |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [List<Models.Vault>](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/vault.md).


# Example Usage

```csharp
string filter = "name eq \"Some Vault Name\"";
try
{
    ApiResponse<List<Vault>> result = await vaultsApi.GetVaultsAsync(filter);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is ErrorResponseException)
    {
       // TODO: Handle ErrorResponseException exception here
    }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/exceptions/error-response.md) |



