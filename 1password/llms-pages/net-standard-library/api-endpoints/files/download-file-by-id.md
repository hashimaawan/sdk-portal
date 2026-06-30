# Download File by ID

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0ZSUyRkZpbGVzJTJGRG93bmxvYWRGaWxlQnlJRA

```csharp
DownloadFileByIdAsync(
    Guid vaultUuid,
    Guid itemUuid,
    string fileUuid)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `Guid` | Template, Required | The UUID of the Vault the item is in |
| `itemUuid` | `Guid` | Template, Required | The UUID of the Item the File is in |
| `fileUuid` | `string` | Template, Required | UUID of the file to get content from |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type Stream.


# Example Usage

```csharp
Guid vaultUuid = new Guid("00002186-0000-0000-0000-000000000000");
Guid itemUuid = new Guid("0000141a-0000-0000-0000-000000000000");
string fileUuid = "fileUuid2";
try
{
    ApiResponse<Stream> result = await filesApi.DownloadFileByIdAsync(
        vaultUuid,
        itemUuid,
        fileUuid
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
| 404 | File not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/exceptions/error-response.md) |



