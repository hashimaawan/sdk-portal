# Teaminfocommon GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/typescript/x-redirect/JTI0ZSUyRiUyRlRlYW1pbmZvY29tbW9uX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```ts
async teaminfocommonGet(
  season: string,
  teamId: string,
  leagueId: string,
  seasonType: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `string` | Query, Required | - |
| `teamId` | `string` | Query, Required | - |
| `leagueId` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const season = 'Season0';

const teamId = 'TeamID8';

const leagueId = 'LeagueID4';

const seasonType = 'SeasonType8';

try {
  const response = await api.teaminfocommonGet(
    season,
    teamId,
    leagueId,
    seasonType
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



