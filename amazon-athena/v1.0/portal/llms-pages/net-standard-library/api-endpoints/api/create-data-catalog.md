# Create Data Catalog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkNyZWF0ZURhdGFDYXRhbG9n

Creates (registers) a data catalog with the specified name and properties. Catalogs created are visible to all users of the same Amazon Web Services account.

```csharp
CreateDataCatalogAsync(
    Models.XAmzTarget3 xAmzTarget,
    Models.CreateDataCatalogInput body,
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
| `xAmzTarget` | [`XAmzTarget3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/x-amz-target-3.md) | Header, Required | - |
| `body` | [`CreateDataCatalogInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/create-data-catalog-input.md) | Body, Required | - |
| `xAmzContentSha256` | `string` | Header, Optional | - |
| `xAmzDate` | `string` | Header, Optional | - |
| `xAmzAlgorithm` | `string` | Header, Optional | - |
| `xAmzCredential` | `string` | Header, Optional | - |
| `xAmzSecurityToken` | `string` | Header, Optional | - |
| `xAmzSignature` | `string` | Header, Optional | - |
| `xAmzSignedHeaders` | `string` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type object.


# Example Usage

```csharp
XAmzTarget3 xAmzTarget = XAmzTarget3.EnumAmazonAthenaCreateDataCatalog;
CreateDataCatalogInput body = new CreateDataCatalogInput
{
    Name = "Name6",
    Type = DataCatalogType1.Hive,
};

try
{
    ApiResponse<object> result = await api.CreateDataCatalogAsync(
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



