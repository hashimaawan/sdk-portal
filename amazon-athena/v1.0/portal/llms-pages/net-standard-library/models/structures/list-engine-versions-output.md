# List Engine Versions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc091dHB1dA


# Class Name

`ListEngineVersionsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EngineVersions` | [`List<EngineVersion>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/engine-version.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

ListEngineVersionsOutput listEngineVersionsOutput = new ListEngineVersionsOutput
{
    EngineVersions = new List<EngineVersion>
    {
        new EngineVersion
        {
            SelectedEngineVersion = "SelectedEngineVersion2",
            EffectiveEngineVersion = "EffectiveEngineVersion2",
        },
    },
    NextToken = "NextToken0",
};
```



