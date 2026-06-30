# Get-Recommendations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlRyYWNrcyUyRmdldC1yZWNvbW1lbmRhdGlvbnM

Recommendations are generated based on the available information for a given seed entity and matched against similar artists and tracks. If there is sufficient information about the provided seeds, a list of tracks will be returned together with pool size details.

For artists and tracks that are very new or obscure there might not be enough data to generate a list of tracks.

```csharp
GetRecommendationsAsync(
    int? limit = 20,
    string market = null,
    string seedArtists = null,
    string seedGenres = null,
    string seedTracks = null,
    double? minAcousticness = null,
    double? maxAcousticness = null,
    double? targetAcousticness = null,
    double? minDanceability = null,
    double? maxDanceability = null,
    double? targetDanceability = null,
    int? minDurationMs = null,
    int? maxDurationMs = null,
    int? targetDurationMs = null,
    double? minEnergy = null,
    double? maxEnergy = null,
    double? targetEnergy = null,
    double? minInstrumentalness = null,
    double? maxInstrumentalness = null,
    double? targetInstrumentalness = null,
    int? minKey = null,
    int? maxKey = null,
    int? targetKey = null,
    double? minLiveness = null,
    double? maxLiveness = null,
    double? targetLiveness = null,
    double? minLoudness = null,
    double? maxLoudness = null,
    double? targetLoudness = null,
    int? minMode = null,
    int? maxMode = null,
    int? targetMode = null,
    int? minPopularity = null,
    int? maxPopularity = null,
    int? targetPopularity = null,
    double? minSpeechiness = null,
    double? maxSpeechiness = null,
    double? targetSpeechiness = null,
    double? minTempo = null,
    double? maxTempo = null,
    double? targetTempo = null,
    int? minTimeSignature = null,
    int? maxTimeSignature = null,
    int? targetTimeSignature = null,
    double? minValence = null,
    double? maxValence = null,
    double? targetValence = null)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `int?` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `market` | `string` | Query, Optional | - |
| `seedArtists` | `string` | Query, Optional | - |
| `seedGenres` | `string` | Query, Optional | - |
| `seedTracks` | `string` | Query, Optional | - |
| `minAcousticness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxAcousticness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetAcousticness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minDanceability` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxDanceability` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetDanceability` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minDurationMs` | `int?` | Query, Optional | - |
| `maxDurationMs` | `int?` | Query, Optional | - |
| `targetDurationMs` | `int?` | Query, Optional | - |
| `minEnergy` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxEnergy` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetEnergy` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minInstrumentalness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxInstrumentalness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetInstrumentalness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minKey` | `int?` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `maxKey` | `int?` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `targetKey` | `int?` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `minLiveness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxLiveness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetLiveness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minLoudness` | `double?` | Query, Optional | - |
| `maxLoudness` | `double?` | Query, Optional | - |
| `targetLoudness` | `double?` | Query, Optional | - |
| `minMode` | `int?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxMode` | `int?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetMode` | `int?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minPopularity` | `int?` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `maxPopularity` | `int?` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `targetPopularity` | `int?` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `minSpeechiness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxSpeechiness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetSpeechiness` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minTempo` | `double?` | Query, Optional | - |
| `maxTempo` | `double?` | Query, Optional | - |
| `targetTempo` | `double?` | Query, Optional | - |
| `minTimeSignature` | `int?` | Query, Optional | **Constraints**: `<= 11` |
| `maxTimeSignature` | `int?` | Query, Optional | - |
| `targetTimeSignature` | `int?` | Query, Optional | - |
| `minValence` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxValence` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetValence` | `double?` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |


# Response Type

**200**: A set of recommendations

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.RecommendationsObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/recommendations-object.md).


# Example Usage

```csharp
int? limit = 10;
string market = "ES";
string seedArtists = "4NHQUGzhtTLFvgF5SZesLK";
string seedGenres = "classical,country";
string seedTracks = "0c6xIDDpzE81m2q797ordA";
try
{
    ApiResponse<RecommendationsObject> result = await tracksApi.GetRecommendationsAsync(
        limit,
        market,
        seedArtists,
        seedGenres,
        seedTracks
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/exceptions/too-many-requests.md) |



