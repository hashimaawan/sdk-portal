# Shotchartlineupdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/typescript/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGxpbmV1cGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```ts
async shotchartlineupdetailGet(
  leagueId: string,
  season: string,
  seasonType: string,
  teamId: string,
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
  gameId: string,
  groupId: string,
  contextMeasure: string,
  contextFilter: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `teamId` | `string` | Query, Required | - |
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
| `gameId` | `string` | Query, Required | - |
| `groupId` | `string` | Query, Required | - |
| `contextMeasure` | `string` | Query, Required | - |
| `contextFilter` | `string` | Query, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const leagueId = 'LeagueID4';

const season = 'Season0';

const seasonType = 'SeasonType8';

const teamId = 'TeamID8';

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

const gameId = 'GameID8';

const groupId = 'GROUP_ID6';

const contextMeasure = 'ContextMeasure2';

const contextFilter = 'ContextFilter6';

try {
  const response = await api.shotchartlineupdetailGet(
    leagueId,
    season,
    seasonType,
    teamId,
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
    gameId,
    groupId,
    contextMeasure,
    contextFilter
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



