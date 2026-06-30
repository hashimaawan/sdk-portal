# Include External

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkluY2x1ZGUlMjUyMEV4dGVybmFs

If `include_external=audio` is specified it signals that the client can play externally hosted audio content, and marks
the content as playable in the response. By default externally hosted audio content is marked as unplayable in the response.


# Enum Type Name

`IncludeExternal`


# Fields

| Name |
|  --- |
| `Audio` |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;

IncludeExternal includeExternal = IncludeExternal.Audio;
```



