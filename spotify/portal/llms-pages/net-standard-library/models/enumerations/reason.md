# Reason

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlYXNvbg

The reason for the restriction. Albums may be restricted if the content is not available in a given market, to the user's subscription type, or when the user's account is set to not play explicit content.
Additional reasons may be added in the future.


# Enum Type Name

`Reason`


# Fields

| Name |
|  --- |
| `Market` |
| `Product` |
| `Explicit` |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;

Reason reason = Reason.Product;
```



