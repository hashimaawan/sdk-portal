# Get-Recommendations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/java/x-redirect/JTI0ZSUyRlRyYWNrcyUyRmdldC1yZWNvbW1lbmRhdGlvbnM

Recommendations are generated based on the available information for a given seed entity and matched against similar artists and tracks. If there is sufficient information about the provided seeds, a list of tracks will be returned together with pool size details.

For artists and tracks that are very new or obscure there might not be enough data to generate a list of tracks.

```java
CompletableFuture<ApiResponse<RecommendationsObject>> getRecommendationsAsync(
    final Integer limit,
    final String market,
    final String seedArtists,
    final String seedGenres,
    final String seedTracks,
    final Double minAcousticness,
    final Double maxAcousticness,
    final Double targetAcousticness,
    final Double minDanceability,
    final Double maxDanceability,
    final Double targetDanceability,
    final Integer minDurationMs,
    final Integer maxDurationMs,
    final Integer targetDurationMs,
    final Double minEnergy,
    final Double maxEnergy,
    final Double targetEnergy,
    final Double minInstrumentalness,
    final Double maxInstrumentalness,
    final Double targetInstrumentalness,
    final Integer minKey,
    final Integer maxKey,
    final Integer targetKey,
    final Double minLiveness,
    final Double maxLiveness,
    final Double targetLiveness,
    final Double minLoudness,
    final Double maxLoudness,
    final Double targetLoudness,
    final Integer minMode,
    final Integer maxMode,
    final Integer targetMode,
    final Integer minPopularity,
    final Integer maxPopularity,
    final Integer targetPopularity,
    final Double minSpeechiness,
    final Double maxSpeechiness,
    final Double targetSpeechiness,
    final Double minTempo,
    final Double maxTempo,
    final Double targetTempo,
    final Integer minTimeSignature,
    final Integer maxTimeSignature,
    final Integer targetTimeSignature,
    final Double minValence,
    final Double maxValence,
    final Double targetValence)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `Integer` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `market` | `String` | Query, Optional | - |
| `seedArtists` | `String` | Query, Optional | - |
| `seedGenres` | `String` | Query, Optional | - |
| `seedTracks` | `String` | Query, Optional | - |
| `minAcousticness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxAcousticness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetAcousticness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minDanceability` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxDanceability` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetDanceability` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minDurationMs` | `Integer` | Query, Optional | - |
| `maxDurationMs` | `Integer` | Query, Optional | - |
| `targetDurationMs` | `Integer` | Query, Optional | - |
| `minEnergy` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxEnergy` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetEnergy` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minInstrumentalness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxInstrumentalness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetInstrumentalness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minKey` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `maxKey` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `targetKey` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `minLiveness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxLiveness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetLiveness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minLoudness` | `Double` | Query, Optional | - |
| `maxLoudness` | `Double` | Query, Optional | - |
| `targetLoudness` | `Double` | Query, Optional | - |
| `minMode` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxMode` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetMode` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minPopularity` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `maxPopularity` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `targetPopularity` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `minSpeechiness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxSpeechiness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetSpeechiness` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minTempo` | `Double` | Query, Optional | - |
| `maxTempo` | `Double` | Query, Optional | - |
| `targetTempo` | `Double` | Query, Optional | - |
| `minTimeSignature` | `Integer` | Query, Optional | **Constraints**: `<= 11` |
| `maxTimeSignature` | `Integer` | Query, Optional | - |
| `targetTimeSignature` | `Integer` | Query, Optional | - |
| `minValence` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxValence` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetValence` | `Double` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |


# Response Type

**200**: A set of recommendations

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`RecommendationsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/structures/recommendations-object.md).


# Example Usage

```java
Integer limit = 10;
String market = "ES";
String seedArtists = "4NHQUGzhtTLFvgF5SZesLK";
String seedGenres = "classical,country";
String seedTracks = "0c6xIDDpzE81m2q797ordA";

tracksApi.getRecommendationsAsync(limit, market, seedArtists, seedGenres, seedTracks, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof UnauthorizedException) {
        UnauthorizedException unauthorizedException = (UnauthorizedException) cause;
        unauthorizedException.printStackTrace();
    } else if (cause instanceof ForbiddenException) {
        ForbiddenException forbiddenException = (ForbiddenException) cause;
        forbiddenException.printStackTrace();
    } else if (cause instanceof TooManyRequestsException) {
        TooManyRequestsException tooManyRequestsException = (TooManyRequestsException) cause;
        tooManyRequestsException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/exceptions/too-many-requests.md) |



