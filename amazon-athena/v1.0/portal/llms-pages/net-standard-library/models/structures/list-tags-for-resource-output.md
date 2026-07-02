# List Tags for Resource Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VPdXRwdXQ

*This model accepts additional fields of type object.*


# Class Name

`ListTagsForResourceOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tags` | [`List<Tag>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/tag.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

ListTagsForResourceOutput listTagsForResourceOutput = new ListTagsForResourceOutput
{
    Tags = new List<Tag>
    {
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    NextToken = "NextToken4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



