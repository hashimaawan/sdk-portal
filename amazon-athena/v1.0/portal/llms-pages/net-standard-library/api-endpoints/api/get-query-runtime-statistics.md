# Get Query Runtime Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3M

Returns query execution runtime statistics related to a single execution of a query if you have access to the workgroup in which the query ran. Query execution runtime statistics are returned only when <a>QueryExecutionStatus$State</a> is in a SUCCEEDED or FAILED state. Stage-level input and output row count and data size statistics are not shown when a query has row-level filters defined in Lake Formation.

```csharp
GetQueryRuntimeStatisticsAsync(
    Models.XAmzTarget25Enum xAmzTarget,
    Models.GetQueryRuntimeStatisticsInput body,
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
| `xAmzTarget` | [`XAmzTarget25Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/x-amz-target-25.md) | Header, Required | - |
| `body` | [`GetQueryRuntimeStatisticsInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/get-query-runtime-statistics-input.md) | Body, Required | - |
| `xAmzContentSha256` | `string` | Header, Optional | - |
| `xAmzDate` | `string` | Header, Optional | - |
| `xAmzAlgorithm` | `string` | Header, Optional | - |
| `xAmzCredential` | `string` | Header, Optional | - |
| `xAmzSecurityToken` | `string` | Header, Optional | - |
| `xAmzSignature` | `string` | Header, Optional | - |
| `xAmzSignedHeaders` | `string` | Header, Optional | - |


# Response Type

**200**: Success

[`Task<Models.GetQueryRuntimeStatisticsOutput>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/get-query-runtime-statistics-output.md)


# Example Usage

```csharp
XAmzTarget25Enum xAmzTarget = XAmzTarget25Enum.EnumAmazonAthenaGetQueryRuntimeStatistics;
GetQueryRuntimeStatisticsInput body = new GetQueryRuntimeStatisticsInput
{
    QueryExecutionId = "QueryExecutionId0",
};

try
{
    GetQueryRuntimeStatisticsOutput result = await aPIController.GetQueryRuntimeStatisticsAsync(
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



