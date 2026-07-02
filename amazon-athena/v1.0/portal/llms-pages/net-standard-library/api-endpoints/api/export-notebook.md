# Export Notebook

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkV4cG9ydE5vdGVib29r

Exports the specified notebook and its metadata.

```csharp
ExportNotebookAsync(
    Models.XAmzTarget14 xAmzTarget,
    Models.ExportNotebookInput body,
    string xAmzContentSha256 = null,
    string xAmzDate = null,
    string xAmzAlgorithm = null,
    string xAmzCredential = null,
    string xAmzSecurityToken = null,
    string xAmzSignature = null,
    string xAmzSignedHeaders = null)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`XAmzTarget14`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/x-amz-target-14.md) | Header, Required | - |
| `body` | [`ExportNotebookInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/export-notebook-input.md) | Body, Required | - |
| `xAmzContentSha256` | `string` | Header, Optional | - |
| `xAmzDate` | `string` | Header, Optional | - |
| `xAmzAlgorithm` | `string` | Header, Optional | - |
| `xAmzCredential` | `string` | Header, Optional | - |
| `xAmzSecurityToken` | `string` | Header, Optional | - |
| `xAmzSignature` | `string` | Header, Optional | - |
| `xAmzSignedHeaders` | `string` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ExportNotebookOutput](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/export-notebook-output.md).


# Example Usage

```csharp
XAmzTarget14 xAmzTarget = XAmzTarget14.EnumAmazonAthenaExportNotebook;
ExportNotebookInput body = new ExportNotebookInput
{
    NotebookId = "NotebookId6",
};

try
{
    ApiResponse<ExportNotebookOutput> result = await api.ExportNotebookAsync(
        xAmzTarget,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiException` |
| 481 | InvalidRequestException | `ApiException` |
| 482 | TooManyRequestsException | `ApiException` |



