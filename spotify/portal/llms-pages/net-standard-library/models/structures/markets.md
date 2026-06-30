# Markets

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1hcmtldHM

*This model accepts additional fields of type object.*


# Class Name

`Markets`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Markets` | `List<string>` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

Markets markets = new Markets
{
    Markets = new List<string>
    {
        "CA",
        "BR",
        "IT",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



