# Followers Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkZvbGxvd2Vyc09iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`FollowersObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Optional | This will always be set to null, as the Web API does not support it at the moment. |
| `Total` | `int?` | Optional | The total number of followers. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

FollowersObject followersObject = new FollowersObject
{
    Href = "href2",
    Total = 62,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



