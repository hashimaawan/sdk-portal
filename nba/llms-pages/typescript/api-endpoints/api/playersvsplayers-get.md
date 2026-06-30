# Playersvsplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/typescript/x-redirect/JTI0ZSUyRiUyRlBsYXllcnN2c3BsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ts
async playersvsplayersGET(
  playerTeamID: string,
  playerID1: string,
  playerID2: string,
  playerID3: string,
  playerID4: string,
  playerID5: string,
  vsTeamID: string,
  vsPlayerID1: string,
  vsPlayerID2: string,
  vsPlayerID3: string,
  vsPlayerID4: string,
  vsPlayerID5: string,
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
  opponentTeamID: string,
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
| `playerTeamID` | `string` | Query, Required | - |
| `playerID1` | `string` | Query, Required | - |
| `playerID2` | `string` | Query, Required | - |
| `playerID3` | `string` | Query, Required | - |
| `playerID4` | `string` | Query, Required | - |
| `playerID5` | `string` | Query, Required | - |
| `vsTeamID` | `string` | Query, Required | - |
| `vsPlayerID1` | `string` | Query, Required | - |
| `vsPlayerID2` | `string` | Query, Required | - |
| `vsPlayerID3` | `string` | Query, Required | - |
| `vsPlayerID4` | `string` | Query, Required | - |
| `vsPlayerID5` | `string` | Query, Required | - |
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
| `opponentTeamID` | `string` | Query, Required | - |
| `vsConference` | `string` | Query, Required | - |
| `vsDivision` | `string` | Query, Required | - |
| `gameSegment` | `string` | Query, Required | - |
| `period` | `string` | Query, Required | - |
| `lastNGames` | `string` | Query, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const playerTeamID = 'PlayerTeamID4';

const playerID1 = 'PlayerID18';

const playerID2 = 'PlayerID24';

const playerID3 = 'PlayerID32';

const playerID4 = 'PlayerID44';

const playerID5 = 'PlayerID54';

const vsTeamID = 'VsTeamID8';

const vsPlayerID1 = 'VsPlayerID12';

const vsPlayerID2 = 'VsPlayerID28';

const vsPlayerID3 = 'VsPlayerID38';

const vsPlayerID4 = 'VsPlayerID46';

const vsPlayerID5 = 'VsPlayerID56';

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

const opponentTeamID = 'OpponentTeamID6';

const vsConference = 'VsConference6';

const vsDivision = 'VsDivision6';

const gameSegment = 'GameSegment6';

const period = 'Period2';

const lastNGames = 'LastNGames4';

try {
  const response = await apiController.playersvsplayersGET(
    playerTeamID,
    playerID1,
    playerID2,
    playerID3,
    playerID4,
    playerID5,
    vsTeamID,
    vsPlayerID1,
    vsPlayerID2,
    vsPlayerID3,
    vsPlayerID4,
    vsPlayerID5,
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
    opponentTeamID,
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



