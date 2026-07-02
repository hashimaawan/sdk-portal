# List Engine Versions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkxpc3RFbmdpbmVWZXJzaW9ucw

Returns a list of engine versions that are available to choose from, including the Auto option.

```csharp
ListEngineVersionsAsync(
    Models.XAmzTarget35Enum xAmzTarget,
    Models.ListEngineVersionsInput body,
    string xAmzContentSha256 = null,
    string xAmzDate = null,
    string xAmzAlgorithm = null,
    string xAmzCredential = null,
    string xAmzSecurityToken = null,
    string xAmzSignature = null,
    string xAmzSignedHeaders = null,
    string maxResults = null,
    string nextToken = null)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`XAmzTarget35Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/x-amz-target-35.md) | Header, Required | - |
| `body` | [`ListEngineVersionsInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/list-engine-versions-input.md) | Body, Required | - |
| `xAmzContentSha256` | `string` | Header, Optional | - |
| `xAmzDate` | `string` | Header, Optional | - |
| `xAmzAlgorithm` | `string` | Header, Optional | - |
| `xAmzCredential` | `string` | Header, Optional | - |
| `xAmzSecurityToken` | `string` | Header, Optional | - |
| `xAmzSignature` | `string` | Header, Optional | - |
| `xAmzSignedHeaders` | `string` | Header, Optional | - |
| `maxResults` | `string` | Query, Optional | Pagination limit |
| `nextToken` | `string` | Query, Optional | Pagination token |


# Response Type

**200**: Success

[`Task<Models.ListEngineVersionsOutput>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/list-engine-versions-output.md)


# Example Usage

```csharp
XAmzTarget35Enum xAmzTarget = XAmzTarget35Enum.EnumAmazonAthenaListEngineVersions;
ListEngineVersionsInput body = new ListEngineVersionsInput
{
};

try
{
    ListEngineVersionsOutput result = await aPIController.ListEngineVersionsAsync(
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



