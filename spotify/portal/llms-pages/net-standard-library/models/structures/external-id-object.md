# External Id Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkV4dGVybmFsSWRPYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`ExternalIdObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Isrc` | `string` | Optional | [International Standard Recording Code](http://en.wikipedia.org/wiki/International_Standard_Recording_Code) |
| `Ean` | `string` | Optional | [International Article Number](http://en.wikipedia.org/wiki/International_Article_Number_%28EAN%29) |
| `Upc` | `string` | Optional | [Universal Product Code](http://en.wikipedia.org/wiki/Universal_Product_Code) |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

ExternalIdObject externalIdObject = new ExternalIdObject
{
    Isrc = "isrc4",
    Ean = "ean2",
    Upc = "upc6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



