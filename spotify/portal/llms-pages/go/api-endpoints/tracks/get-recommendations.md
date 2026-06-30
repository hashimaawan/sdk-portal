# Get-Recommendations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0ZSUyRlRyYWNrcyUyRmdldC1yZWNvbW1lbmRhdGlvbnM

Recommendations are generated based on the available information for a given seed entity and matched against similar artists and tracks. If there is sufficient information about the provided seeds, a list of tracks will be returned together with pool size details.

For artists and tracks that are very new or obscure there might not be enough data to generate a list of tracks.

```go
GetRecommendations(
    ctx context.Context,
    limit *int,
    market *string,
    seedArtists *string,
    seedGenres *string,
    seedTracks *string,
    minAcousticness *float64,
    maxAcousticness *float64,
    targetAcousticness *float64,
    minDanceability *float64,
    maxDanceability *float64,
    targetDanceability *float64,
    minDurationMs *int,
    maxDurationMs *int,
    targetDurationMs *int,
    minEnergy *float64,
    maxEnergy *float64,
    targetEnergy *float64,
    minInstrumentalness *float64,
    maxInstrumentalness *float64,
    targetInstrumentalness *float64,
    minKey *int,
    maxKey *int,
    targetKey *int,
    minLiveness *float64,
    maxLiveness *float64,
    targetLiveness *float64,
    minLoudness *float64,
    maxLoudness *float64,
    targetLoudness *float64,
    minMode *int,
    maxMode *int,
    targetMode *int,
    minPopularity *int,
    maxPopularity *int,
    targetPopularity *int,
    minSpeechiness *float64,
    maxSpeechiness *float64,
    targetSpeechiness *float64,
    minTempo *float64,
    maxTempo *float64,
    targetTempo *float64,
    minTimeSignature *int,
    maxTimeSignature *int,
    targetTimeSignature *int,
    minValence *float64,
    maxValence *float64,
    targetValence *float64) (
    models.ApiResponse[models.RecommendationsObject],
    error)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `*int` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `market` | `*string` | Query, Optional | - |
| `seedArtists` | `*string` | Query, Optional | - |
| `seedGenres` | `*string` | Query, Optional | - |
| `seedTracks` | `*string` | Query, Optional | - |
| `minAcousticness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxAcousticness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetAcousticness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minDanceability` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxDanceability` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetDanceability` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minDurationMs` | `*int` | Query, Optional | - |
| `maxDurationMs` | `*int` | Query, Optional | - |
| `targetDurationMs` | `*int` | Query, Optional | - |
| `minEnergy` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxEnergy` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetEnergy` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minInstrumentalness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxInstrumentalness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetInstrumentalness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minKey` | `*int` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `maxKey` | `*int` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `targetKey` | `*int` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `minLiveness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxLiveness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetLiveness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minLoudness` | `*float64` | Query, Optional | - |
| `maxLoudness` | `*float64` | Query, Optional | - |
| `targetLoudness` | `*float64` | Query, Optional | - |
| `minMode` | `*int` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxMode` | `*int` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetMode` | `*int` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minPopularity` | `*int` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `maxPopularity` | `*int` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `targetPopularity` | `*int` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `minSpeechiness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxSpeechiness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetSpeechiness` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minTempo` | `*float64` | Query, Optional | - |
| `maxTempo` | `*float64` | Query, Optional | - |
| `targetTempo` | `*float64` | Query, Optional | - |
| `minTimeSignature` | `*int` | Query, Optional | **Constraints**: `<= 11` |
| `maxTimeSignature` | `*int` | Query, Optional | - |
| `targetTimeSignature` | `*int` | Query, Optional | - |
| `minValence` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxValence` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetValence` | `*float64` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |


# Response Type

**200**: A set of recommendations

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.RecommendationsObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/recommendations-object.md).


# Example Usage

```go
ctx := context.Background()

limit := 10

market := "ES"

seedArtists := "4NHQUGzhtTLFvgF5SZesLK"

seedGenres := "classical,country"

seedTracks := "0c6xIDDpzE81m2q797ordA"

apiResponse, err := tracksApi.GetRecommendations(ctx, &limit, &market, &seedArtists, &seedGenres, &seedTracks, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.Unauthorized:
            log.Fatalln("UnauthorizedException: ", typedErr)
        case *errors.Forbidden:
            log.Fatalln("ForbiddenException: ", typedErr)
        case *errors.TooManyRequests:
            log.Fatalln("TooManyRequestsException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/exceptions/too-many-requests.md) |



