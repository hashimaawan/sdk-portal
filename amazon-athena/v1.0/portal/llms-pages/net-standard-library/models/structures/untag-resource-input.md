# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResourceARN` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `TagKeys` | `List<string>` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

UntagResourceInput untagResourceInput = new UntagResourceInput
{
    ResourceARN = "ResourceARN6",
    TagKeys = new List<string>
    {
        "TagKeys1",
        "TagKeys2",
        "TagKeys3",
    },
};
```



