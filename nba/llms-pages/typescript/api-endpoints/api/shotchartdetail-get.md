# Shotchartdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/typescript/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```ts
async shotchartdetailGET(
  seasonType: string,
  teamID: string,
  playerID: string,
  gameID: string,
  outcome: string,
  location: string,
  month: string,
  seasonSegment: string,
  dateFrom: string,
  dateTo: string,
  opponentTeamID: string,
  vsConference: string,
  vsDivision: string,
  position: string,
  rookieYear: string,
  gameSegment: string,
  period: string,
  lastNGames: string,
  contextMeasure: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `seasonType` | `string` | Query, Required | - |
| `teamID` | `string` | Query, Required | - |
| `playerID` | `string` | Query, Required | - |
| `gameID` | `string` | Query, Required | - |
| `outcome` | `string` | Query, Required | - |
| `location` | `string` | Query, Required | - |
| `month` | `string` | Query, Required | - |
| `seasonSegment` | `string` | Query, Required | - |
| `dateFrom` | `string` | Query, Required | - |
| `dateTo` | `string` | Query, Required | - |
| `opponentTeamID` | `string` | Query, Required | - |
| `vsConference` | `string` | Query, Required | - |
| `vsDivision` | `string` | Query, Required | - |
| `position` | `string` | Query, Required | - |
| `rookieYear` | `string` | Query, Required | - |
| `gameSegment` | `string` | Query, Required | - |
| `period` | `string` | Query, Required | - |
| `lastNGames` | `string` | Query, Required | - |
| `contextMeasure` | `string` | Query, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const seasonType = 'SeasonType8';

const teamID = 'TeamID8';

const playerID = 'PlayerID6';

const gameID = 'GameID8';

const outcome = 'Outcome4';

const location = 'Location4';

const month = 'Month0';

const seasonSegment = 'SeasonSegment8';

const dateFrom = 'DateFrom6';

const dateTo = 'DateTo0';

const opponentTeamID = 'OpponentTeamID6';

const vsConference = 'VsConference6';

const vsDivision = 'VsDivision6';

const position = 'Position8';

const rookieYear = 'RookieYear8';

const gameSegment = 'GameSegment6';

const period = 'Period2';

const lastNGames = 'LastNGames4';

const contextMeasure = 'ContextMeasure2';

try {
  const response = await apiController.shotchartdetailGET(
    seasonType,
    teamID,
    playerID,
    gameID,
    outcome,
    location,
    month,
    seasonSegment,
    dateFrom,
    dateTo,
    opponentTeamID,
    vsConference,
    vsDivision,
    position,
    rookieYear,
    gameSegment,
    period,
    lastNGames,
    contextMeasure
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



