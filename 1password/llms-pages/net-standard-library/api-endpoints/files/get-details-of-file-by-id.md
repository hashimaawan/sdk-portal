# Get Details of File by Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0ZSUyRkZpbGVzJTJGR2V0RGV0YWlsc09mRmlsZUJ5SWQ

```csharp
GetDetailsOfFileByIdAsync(
    Guid vaultUuid,
    Guid itemUuid,
    Guid fileUuid,
    bool? inlineFiles = null)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `Guid` | Template, Required | The UUID of the Vault to fetch Item from |
| `itemUuid` | `Guid` | Template, Required | The UUID of the Item to fetch File from |
| `fileUuid` | `Guid` | Template, Required | The UUID of the File to fetch |
| `inlineFiles` | `bool?` | Query, Optional | Tells server to return the base64-encoded file contents in the response. |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.File](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/file.md).


# Example Usage

```csharp
Guid vaultUuid = new Guid("00002186-0000-0000-0000-000000000000");
Guid itemUuid = new Guid("0000141a-0000-0000-0000-000000000000");
Guid fileUuid = new Guid("000008e0-0000-0000-0000-000000000000");
bool? inlineFiles = true;
try
{
    ApiResponse<File> result = await filesApi.GetDetailsOfFileByIdAsync(
        vaultUuid,
        itemUuid,
        fileUuid,
        inlineFiles
    );
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
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/exceptions/error-response.md) |
| 404 | File not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/exceptions/error-response.md) |
| 413 | File content too large to display | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/exceptions/error-response.md) |



