# Get-Recommendations

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0ZSUyRlRyYWNrcyUyRmdldC1yZWNvbW1lbmRhdGlvbnM

Recommendations are generated based on the available information for a given seed entity and matched against similar artists and tracks. If there is sufficient information about the provided seeds, a list of tracks will be returned together with pool size details.

For artists and tracks that are very new or obscure there might not be enough data to generate a list of tracks.

```ts
async getRecommendations(
  limit?: number,
  market?: string,
  seedArtists?: string,
  seedGenres?: string,
  seedTracks?: string,
  minAcousticness?: number,
  maxAcousticness?: number,
  targetAcousticness?: number,
  minDanceability?: number,
  maxDanceability?: number,
  targetDanceability?: number,
  minDurationMs?: number,
  maxDurationMs?: number,
  targetDurationMs?: number,
  minEnergy?: number,
  maxEnergy?: number,
  targetEnergy?: number,
  minInstrumentalness?: number,
  maxInstrumentalness?: number,
  targetInstrumentalness?: number,
  minKey?: number,
  maxKey?: number,
  targetKey?: number,
  minLiveness?: number,
  maxLiveness?: number,
  targetLiveness?: number,
  minLoudness?: number,
  maxLoudness?: number,
  targetLoudness?: number,
  minMode?: number,
  maxMode?: number,
  targetMode?: number,
  minPopularity?: number,
  maxPopularity?: number,
  targetPopularity?: number,
  minSpeechiness?: number,
  maxSpeechiness?: number,
  targetSpeechiness?: number,
  minTempo?: number,
  maxTempo?: number,
  targetTempo?: number,
  minTimeSignature?: number,
  maxTimeSignature?: number,
  targetTimeSignature?: number,
  minValence?: number,
  maxValence?: number,
  targetValence?: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<RecommendationsObject>>
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `number \| undefined` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `market` | `string \| undefined` | Query, Optional | - |
| `seedArtists` | `string \| undefined` | Query, Optional | - |
| `seedGenres` | `string \| undefined` | Query, Optional | - |
| `seedTracks` | `string \| undefined` | Query, Optional | - |
| `minAcousticness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxAcousticness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetAcousticness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minDanceability` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxDanceability` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetDanceability` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minDurationMs` | `number \| undefined` | Query, Optional | - |
| `maxDurationMs` | `number \| undefined` | Query, Optional | - |
| `targetDurationMs` | `number \| undefined` | Query, Optional | - |
| `minEnergy` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxEnergy` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetEnergy` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minInstrumentalness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxInstrumentalness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetInstrumentalness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minKey` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `maxKey` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `targetKey` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `minLiveness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxLiveness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetLiveness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minLoudness` | `number \| undefined` | Query, Optional | - |
| `maxLoudness` | `number \| undefined` | Query, Optional | - |
| `targetLoudness` | `number \| undefined` | Query, Optional | - |
| `minMode` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxMode` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetMode` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minPopularity` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `maxPopularity` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `targetPopularity` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `minSpeechiness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxSpeechiness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetSpeechiness` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `minTempo` | `number \| undefined` | Query, Optional | - |
| `maxTempo` | `number \| undefined` | Query, Optional | - |
| `targetTempo` | `number \| undefined` | Query, Optional | - |
| `minTimeSignature` | `number \| undefined` | Query, Optional | **Constraints**: `<= 11` |
| `maxTimeSignature` | `number \| undefined` | Query, Optional | - |
| `targetTimeSignature` | `number \| undefined` | Query, Optional | - |
| `minValence` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `maxValence` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `targetValence` | `number \| undefined` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A set of recommendations

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`RecommendationsObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/recommendations-object.md).


# Example Usage

```ts
const limit = 10;

const market = 'ES';

const seedArtists = '4NHQUGzhtTLFvgF5SZesLK';

const seedGenres = 'classical,country';

const seedTracks = '0c6xIDDpzE81m2q797ordA';

try {
  const response = await tracksApi.getRecommendations(
    limit,
    market,
    seedArtists,
    seedGenres,
    seedTracks
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
    if (error instanceof UnauthorizedError) {
      console.log(error.result);
    } else if (error instanceof ForbiddenError) {
      console.log(error.result);
    } else if (error instanceof TooManyRequestsError) {
      console.log(error.result);
    }
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedError`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenError`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsError`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/exceptions/too-many-requests.md) |



