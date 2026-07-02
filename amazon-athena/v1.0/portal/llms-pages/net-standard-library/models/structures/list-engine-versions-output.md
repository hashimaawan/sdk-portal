# List Engine Versions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc091dHB1dA

*This model accepts additional fields of type object.*


# Class Name

`ListEngineVersionsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EngineVersions` | [`List<EngineVersion>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/engine-version.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

ListEngineVersionsOutput listEngineVersionsOutput = new ListEngineVersionsOutput
{
    EngineVersions = new List<EngineVersion>
    {
        new EngineVersion
        {
            SelectedEngineVersion = "SelectedEngineVersion2",
            EffectiveEngineVersion = "EffectiveEngineVersion2",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    NextToken = "NextToken0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



