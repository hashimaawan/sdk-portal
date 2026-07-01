# Leaguedashteamshotlocations GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/typescript/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2h0ZWFtc2hvdGxvY2F0aW9uc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```ts
async leaguedashteamshotlocationsGet(
  measureType: string,
  perMode: string,
  plusMinus: string,
  paceAdjust: string,
  rank: string,
  season: string,
  seasonType: string,
  outcome: string,
  location: string,
  month: string,
  seasonSegment: string,
  dateFrom: string,
  dateTo: string,
  opponentTeamId: string,
  vsConference: string,
  vsDivision: string,
  gameSegment: string,
  period: string,
  lastNGames: string,
  distanceRange: string,
  gameScope: string,
  playerExperience: string,
  playerPosition: string,
  starterBench: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `measureType` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `plusMinus` | `string` | Query, Required | - |
| `paceAdjust` | `string` | Query, Required | - |
| `rank` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `outcome` | `string` | Query, Required | - |
| `location` | `string` | Query, Required | - |
| `month` | `string` | Query, Required | - |
| `seasonSegment` | `string` | Query, Required | - |
| `dateFrom` | `string` | Query, Required | - |
| `dateTo` | `string` | Query, Required | - |
| `opponentTeamId` | `string` | Query, Required | - |
| `vsConference` | `string` | Query, Required | - |
| `vsDivision` | `string` | Query, Required | - |
| `gameSegment` | `string` | Query, Required | - |
| `period` | `string` | Query, Required | - |
| `lastNGames` | `string` | Query, Required | - |
| `distanceRange` | `string` | Query, Required | - |
| `gameScope` | `string` | Query, Required | - |
| `playerExperience` | `string` | Query, Required | - |
| `playerPosition` | `string` | Query, Required | - |
| `starterBench` | `string` | Query, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const measureType = 'MeasureType8';

const perMode = 'PerMode6';

const plusMinus = 'PlusMinus0';

const paceAdjust = 'PaceAdjust2';

const rank = 'Rank2';

const season = 'Season0';

const seasonType = 'SeasonType8';

const outcome = 'Outcome4';

const location = 'Location4';

const month = 'Month0';

const seasonSegment = 'SeasonSegment8';

const dateFrom = 'DateFrom6';

const dateTo = 'DateTo0';

const opponentTeamId = 'OpponentTeamID6';

const vsConference = 'VsConference6';

const vsDivision = 'VsDivision6';

const gameSegment = 'GameSegment6';

const period = 'Period2';

const lastNGames = 'LastNGames4';

const distanceRange = 'DistanceRange6';

const gameScope = 'GameScope0';

const playerExperience = 'PlayerExperience4';

const playerPosition = 'PlayerPosition8';

const starterBench = 'StarterBench0';

try {
  const response = await api.leaguedashteamshotlocationsGet(
    measureType,
    perMode,
    plusMinus,
    paceAdjust,
    rank,
    season,
    seasonType,
    outcome,
    location,
    month,
    seasonSegment,
    dateFrom,
    dateTo,
    opponentTeamId,
    vsConference,
    vsDivision,
    gameSegment,
    period,
    lastNGames,
    distanceRange,
    gameScope,
    playerExperience,
    playerPosition,
    starterBench
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
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiError` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiError` |



