# List Tags for Resource Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VPdXRwdXQ


# Class Name

`ListTagsForResourceOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tags` | [`List<Tag>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/tag.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

ListTagsForResourceOutput listTagsForResourceOutput = new ListTagsForResourceOutput
{
    Tags = new List<Tag>
    {
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
        },
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
        },
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
        },
    },
    NextToken = "NextToken4",
};
```



