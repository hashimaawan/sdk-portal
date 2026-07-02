# List Application DPU Sizes Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzSW5wdXQ

*This model accepts additional fields of type object.*


# Class Name

`ListApplicationDpuSizesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ListApplicationDpuSizesInput listApplicationDpuSizesInput = new ListApplicationDpuSizesInput
{
    MaxResults = 56,
    NextToken = "NextToken6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



