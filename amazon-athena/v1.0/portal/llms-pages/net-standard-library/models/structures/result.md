# Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdA

*This model accepts additional fields of type object.*


# Class Name

`Result`


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

Result result = new Result
{
    StdOutS3Uri = "StdOutS3Uri8",
    StdErrorS3Uri = "StdErrorS3Uri0",
    ResultS3Uri = "ResultS3Uri4",
    ResultType = "ResultType6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



