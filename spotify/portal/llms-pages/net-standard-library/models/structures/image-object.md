# Image Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdlT2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`ImageObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Url` | `string` | Required | The source URL of the image. |
| `Height` | `int?` | Required | The image height in pixels. |
| `Width` | `int?` | Required | The image width in pixels. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

ImageObject imageObject = new ImageObject
{
    Url = "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
    Height = 300,
    Width = 300,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



