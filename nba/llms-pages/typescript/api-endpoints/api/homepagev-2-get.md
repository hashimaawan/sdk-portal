# Homepagev 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/typescript/x-redirect/JTI0ZSUyRiUyRkhvbWVwYWdldjJfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ts
async homepagev2GET(
  statType: string,
  leagueID: string,
  season: string,
  seasonType: string,
  playerOrTeam: string,
  playerScope: string,
  gameScope: string,
  game?: string,
  player?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statType` | `string` | Query, Required | - |
| `leagueID` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `playerOrTeam` | `string` | Query, Required | - |
| `playerScope` | `string` | Query, Required | - |
| `gameScope` | `string` | Query, Required | - |
| `game` | `string \| undefined` | Query, Optional | - |
| `player` | `string \| undefined` | Query, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const statType = 'StatType8';

const leagueID = 'LeagueID4';

const season = 'Season0';

const seasonType = 'SeasonType8';

const playerOrTeam = 'PlayerOrTeam8';

const playerScope = 'PlayerScope2';

const gameScope = 'GameScope0';

try {
  const response = await apiController.homepagev2GET(
    statType,
    leagueID,
    season,
    seasonType,
    playerOrTeam,
    playerScope,
    gameScope
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



