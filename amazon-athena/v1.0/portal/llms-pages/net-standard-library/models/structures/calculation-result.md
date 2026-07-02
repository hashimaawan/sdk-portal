# Calculation Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uUmVzdWx0

Contains information about an application-specific calculation result.

*This model accepts additional fields of type object.*


# Class Name

`CalculationResult`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StdOutS3Uri` | `string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `StdErrorS3Uri` | `string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `ResultS3Uri` | `string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `ResultType` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `\w+\/[-+.\w]+` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

CalculationResult calculationResult = new CalculationResult
{
    StdOutS3Uri = "StdOutS3Uri4",
    StdErrorS3Uri = "StdErrorS3Uri6",
    ResultS3Uri = "ResultS3Uri0",
    ResultType = "ResultType2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



