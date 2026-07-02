# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type object.*


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResourceArn` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `TagKeys` | `List<string>` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

UntagResourceInput untagResourceInput = new UntagResourceInput
{
    ResourceArn = "ResourceARN6",
    TagKeys = new List<string>
    {
        "TagKeys1",
        "TagKeys2",
        "TagKeys3",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



