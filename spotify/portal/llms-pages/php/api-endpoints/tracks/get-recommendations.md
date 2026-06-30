# Get-Recommendations

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/php/x-redirect/JTI0ZSUyRlRyYWNrcyUyRmdldC1yZWNvbW1lbmRhdGlvbnM

Recommendations are generated based on the available information for a given seed entity and matched against similar artists and tracks. If there is sufficient information about the provided seeds, a list of tracks will be returned together with pool size details.

For artists and tracks that are very new or obscure there might not be enough data to generate a list of tracks.

```php
function getRecommendations(
    ?int $limit = 20,
    ?string $market = null,
    ?string $seedArtists = null,
    ?string $seedGenres = null,
    ?string $seedTracks = null,
    ?float $minAcousticness = null,
    ?float $maxAcousticness = null,
    ?float $targetAcousticness = null,
    ?float $minDanceability = null,
    ?float $maxDanceability = null,
    ?float $targetDanceability = null,
    ?int $minDurationMs = null,
    ?int $maxDurationMs = null,
    ?int $targetDurationMs = null,
    ?float $minEnergy = null,
    ?float $maxEnergy = null,
    ?float $targetEnergy = null,
    ?float $minInstrumentalness = null,
    ?float $maxInstrumentalness = null,
    ?float $targetInstrumentalness = null,
    ?int $minKey = null,
    ?int $maxKey = null,
    ?int $targetKey = null,
    ?float $minLiveness = null,
    ?float $maxLiveness = null,
    ?float $targetLiveness = null,
    ?float $minLoudness = null,
    ?float $maxLoudness = null,
    ?float $targetLoudness = null,
    ?int $minMode = null,
    ?int $maxMode = null,
    ?int $targetMode = null,
    ?int $minPopularity = null,
    ?int $maxPopularity = null,
    ?int $targetPopularity = null,
    ?float $minSpeechiness = null,
    ?float $maxSpeechiness = null,
    ?float $targetSpeechiness = null,
    ?float $minTempo = null,
    ?float $maxTempo = null,
    ?float $targetTempo = null,
    ?int $minTimeSignature = null,
    ?int $maxTimeSignature = null,
    ?int $targetTimeSignature = null,
    ?float $minValence = null,
    ?float $maxValence = null,
    ?float $targetValence = null
): ApiResponse
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `?int` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `market` | `?string` | Query, Optional | - |
| `seedArtists` | `?string` | Query, Optional | - |
| `seedGenres` | `?string` | Query, Optional | - |
| `seedTracks` | `?string` | Query, Optional | - |
| `minAcousticness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxAcousticness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetAcousticness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minDanceability` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxDanceability` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetDanceability` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minDurationMs` | `?int` | Query, Optional | - |
| `maxDurationMs` | `?int` | Query, Optional | - |
| `targetDurationMs` | `?int` | Query, Optional | - |
| `minEnergy` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxEnergy` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetEnergy` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minInstrumentalness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxInstrumentalness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetInstrumentalness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minKey` | `?int` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `maxKey` | `?int` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `targetKey` | `?int` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `minLiveness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxLiveness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetLiveness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minLoudness` | `?float` | Query, Optional | - |
| `maxLoudness` | `?float` | Query, Optional | - |
| `targetLoudness` | `?float` | Query, Optional | - |
| `minMode` | `?int` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxMode` | `?int` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetMode` | `?int` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minPopularity` | `?int` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `maxPopularity` | `?int` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `targetPopularity` | `?int` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `minSpeechiness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxSpeechiness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetSpeechiness` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minTempo` | `?float` | Query, Optional | - |
| `maxTempo` | `?float` | Query, Optional | - |
| `targetTempo` | `?float` | Query, Optional | - |
| `minTimeSignature` | `?int` | Query, Optional | **Constraints**: `<= 11` |
| `maxTimeSignature` | `?int` | Query, Optional | - |
| `targetTimeSignature` | `?int` | Query, Optional | - |
| `minValence` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxValence` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetValence` | `?float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |


# Response Type

**200**: A set of recommendations

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`RecommendationsObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/recommendations-object.md).


# Example Usage

```php
$limit = 10;

$market = 'ES';

$seedArtists = '4NHQUGzhtTLFvgF5SZesLK';

$seedGenres = 'classical,country';

$seedTracks = '0c6xIDDpzE81m2q797ordA';

$tracksApi = $client->getTracksApi();
$apiResponse = $tracksApi->getRecommendations(
    $limit,
    $market,
    $seedArtists,
    $seedGenres,
    $seedTracks
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'RecommendationsObject:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/exceptions/too-many-requests.md) |



