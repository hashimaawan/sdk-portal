# Recommendation Seed Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlY29tbWVuZGF0aW9uU2VlZE9iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`RecommendationSeedObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AfterFilteringSize` | `int?` | Optional | The number of tracks available after min\_\* and max\_\* filters have been applied. |
| `AfterRelinkingSize` | `int?` | Optional | The number of tracks available after relinking for regional availability. |
| `Href` | `string` | Optional | A link to the full track or artist data for this seed. For tracks this will be a link to a Track Object. For artists a link to an Artist Object. For genre seeds, this value will be `null`. |
| `Id` | `string` | Optional | The id used to select this seed. This will be the same as the string used in the `seed_artists`, `seed_tracks` or `seed_genres` parameter. |
| `InitialPoolSize` | `int?` | Optional | The number of recommended tracks available for this seed. |
| `Type` | `string` | Optional | The entity type of this seed. One of `artist`, `track` or `genre`. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

RecommendationSeedObject recommendationSeedObject = new RecommendationSeedObject
{
    AfterFilteringSize = 118,
    AfterRelinkingSize = 194,
    Href = "href0",
    Id = "id8",
    InitialPoolSize = 124,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



