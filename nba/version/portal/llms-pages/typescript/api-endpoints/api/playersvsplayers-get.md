# Playersvsplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/typescript/x-redirect/JTI0ZSUyRiUyRlBsYXllcnN2c3BsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ts
async playersvsplayersGet(
  playerTeamId: string,
  playerId1: string,
  playerId2: string,
  playerId3: string,
  playerId4: string,
  playerId5: string,
  vsTeamId: string,
  vsPlayerId1: string,
  vsPlayerId2: string,
  vsPlayerId3: string,
  vsPlayerId4: string,
  vsPlayerId5: string,
  seasonType: string,
  measureType: string,
  perMode: string,
  plusMinus: string,
  paceAdjust: string,
  rank: string,
  season: string,
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
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playerTeamId` | `string` | Query, Required | - |
| `playerId1` | `string` | Query, Required | - |
| `playerId2` | `string` | Query, Required | - |
| `playerId3` | `string` | Query, Required | - |
| `playerId4` | `string` | Query, Required | - |
| `playerId5` | `string` | Query, Required | - |
| `vsTeamId` | `string` | Query, Required | - |
| `vsPlayerId1` | `string` | Query, Required | - |
| `vsPlayerId2` | `string` | Query, Required | - |
| `vsPlayerId3` | `string` | Query, Required | - |
| `vsPlayerId4` | `string` | Query, Required | - |
| `vsPlayerId5` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `measureType` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `plusMinus` | `string` | Query, Required | - |
| `paceAdjust` | `string` | Query, Required | - |
| `rank` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
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
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const playerTeamId = 'PlayerTeamID4';

const playerId1 = 'PlayerID18';

const playerId2 = 'PlayerID24';

const playerId3 = 'PlayerID32';

const playerId4 = 'PlayerID44';

const playerId5 = 'PlayerID54';

const vsTeamId = 'VsTeamID8';

const vsPlayerId1 = 'VsPlayerID12';

const vsPlayerId2 = 'VsPlayerID28';

const vsPlayerId3 = 'VsPlayerID38';

const vsPlayerId4 = 'VsPlayerID46';

const vsPlayerId5 = 'VsPlayerID56';

const seasonType = 'SeasonType8';

const measureType = 'MeasureType8';

const perMode = 'PerMode6';

const plusMinus = 'PlusMinus0';

const paceAdjust = 'PaceAdjust2';

const rank = 'Rank2';

const season = 'Season0';

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

try {
  const response = await api.playersvsplayersGet(
    playerTeamId,
    playerId1,
    playerId2,
    playerId3,
    playerId4,
    playerId5,
    vsTeamId,
    vsPlayerId1,
    vsPlayerId2,
    vsPlayerId3,
    vsPlayerId4,
    vsPlayerId5,
    seasonType,
    measureType,
    perMode,
    plusMinus,
    paceAdjust,
    rank,
    season,
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
    lastNGames
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



