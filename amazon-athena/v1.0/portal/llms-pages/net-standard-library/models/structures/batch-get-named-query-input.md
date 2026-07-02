# Batch Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeUlucHV0

Contains an array of named query IDs.


# Class Name

`BatchGetNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueryIds` | `List<string>` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

BatchGetNamedQueryInput batchGetNamedQueryInput = new BatchGetNamedQueryInput
{
    NamedQueryIds = new List<string>
    {
        "NamedQueryIds3",
        "NamedQueryIds4",
    },
};
```



