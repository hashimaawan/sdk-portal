# Get-Multiple-Shows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0ZSUyRlNob3dzJTJGZ2V0LW11bHRpcGxlLXNob3dz

Get Spotify catalog information for several shows based on their Spotify IDs.

```csharp
GetMultipleShowsAsync(
    string ids,
    string market = null)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `string` | Query, Required | - |
| `market` | `string` | Query, Optional | - |


# Response Type

**200**: A set of shows

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ManySimplifiedShows](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/many-simplified-shows.md).


# Example Usage

```csharp
string ids = "5CfCWKI5pZ28U0uOzXkDHe,5as3aKmN2k11yfDDDSrvaZ";
string market = "ES";
try
{
    ApiResponse<ManySimplifiedShows> result = await showsApi.GetMultipleShowsAsync(
        ids,
        market
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is UnauthorizedException)
    {
       // TODO: Handle UnauthorizedException exception here
    }
    if (e is ForbiddenException)
    {
       // TODO: Handle ForbiddenException exception here
    }
    if (e is TooManyRequestsException)
    {
       // TODO: Handle TooManyRequestsException exception here
    }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/exceptions/too-many-requests.md) |



