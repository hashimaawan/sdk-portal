# Scoreboard V2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/typescript/x-redirect/JTI0ZSUyRiUyRlNjb3JlYm9hcmRWMl9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```ts
async scoreboardV2GET(
  gameDate: string,
  leagueID: string,
  dayOffset: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameDate` | `string` | Query, Required | - |
| `leagueID` | `string` | Query, Required | - |
| `dayOffset` | `string` | Query, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const gameDate = 'GameDate8';

const leagueID = 'LeagueID4';

const dayOffset = 'DayOffset6';

try {
  const response = await apiController.scoreboardV2GET(
    gameDate,
    leagueID,
    dayOffset
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



