# Many Genres

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1hbnlHZW5yZXM

*This model accepts additional fields of type object.*


# Class Name

`ManyGenres`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Genres` | `List<string>` | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

ManyGenres manyGenres = new ManyGenres
{
    Genres = new List<string>
    {
        "alternative",
        "samba",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



