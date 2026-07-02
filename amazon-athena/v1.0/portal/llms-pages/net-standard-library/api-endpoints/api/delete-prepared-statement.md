# Delete Prepared Statement

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkRlbGV0ZVByZXBhcmVkU3RhdGVtZW50

Deletes the prepared statement with the specified name from the specified workgroup.

```csharp
DeletePreparedStatementAsync(
    Models.XAmzTarget12 xAmzTarget,
    Models.DeletePreparedStatementInput body,
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
| `xAmzTarget` | [`XAmzTarget12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/x-amz-target-12.md) | Header, Required | - |
| `body` | [`DeletePreparedStatementInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/delete-prepared-statement-input.md) | Body, Required | - |
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
XAmzTarget12 xAmzTarget = XAmzTarget12.EnumAmazonAthenaDeletePreparedStatement;
DeletePreparedStatementInput body = new DeletePreparedStatementInput
{
    StatementName = "StatementName4",
    WorkGroup = "WorkGroup8",
};

try
{
    ApiResponse<object> result = await api.DeletePreparedStatementAsync(
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
| 482 | ResourceNotFoundException | `ApiException` |



