# Copyright Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkNvcHlyaWdodE9iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`CopyrightObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Text` | `string` | Optional | The copyright text for this content. |
| `Type` | `string` | Optional | The type of copyright: `C` = the copyright, `P` = the sound recording (performance) copyright. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

CopyrightObject copyrightObject = new CopyrightObject
{
    Text = "text4",
    Type = "type4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



