# Playerprofile GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/typescript/x-redirect/JTI0ZSUyRiUyRlBsYXllcnByb2ZpbGVfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ts
async playerprofileGet(
  leagueId: string,
  playerId: string,
  season: string,
  seasonType: string,
  graphStartSeason: string,
  graphEndSeason: string,
  graphStat: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `playerId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `graphStartSeason` | `string` | Query, Required | - |
| `graphEndSeason` | `string` | Query, Required | - |
| `graphStat` | `string` | Query, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const leagueId = 'LeagueID4';

const playerId = 'PlayerID6';

const season = 'Season0';

const seasonType = 'SeasonType8';

const graphStartSeason = 'GraphStartSeason2';

const graphEndSeason = 'GraphEndSeason6';

const graphStat = 'GraphStat0';

try {
  const response = await api.playerprofileGet(
    leagueId,
    playerId,
    season,
    seasonType,
    graphStartSeason,
    graphEndSeason,
    graphStat
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



