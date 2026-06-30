# Playerdashptreboundlogs GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/typescript/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHJlYm91bmRsb2dzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```ts
async playerdashptreboundlogsGET(
  season?: string,
  seasonType?: string,
  playerID?: string,
  teamID?: string,
  outcome?: string,
  location?: string,
  month?: string,
  seasonSegment?: string,
  dateFrom?: string,
  dateTo?: string,
  opponentTeamID?: string,
  vsConference?: string,
  vsDivision?: string,
  gameSegment?: string,
  period?: string,
  lastNGames?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `string \| undefined` | Query, Optional | - |
| `seasonType` | `string \| undefined` | Query, Optional | - |
| `playerID` | `string \| undefined` | Query, Optional | - |
| `teamID` | `string \| undefined` | Query, Optional | - |
| `outcome` | `string \| undefined` | Query, Optional | - |
| `location` | `string \| undefined` | Query, Optional | - |
| `month` | `string \| undefined` | Query, Optional | - |
| `seasonSegment` | `string \| undefined` | Query, Optional | - |
| `dateFrom` | `string \| undefined` | Query, Optional | - |
| `dateTo` | `string \| undefined` | Query, Optional | - |
| `opponentTeamID` | `string \| undefined` | Query, Optional | - |
| `vsConference` | `string \| undefined` | Query, Optional | - |
| `vsDivision` | `string \| undefined` | Query, Optional | - |
| `gameSegment` | `string \| undefined` | Query, Optional | - |
| `period` | `string \| undefined` | Query, Optional | - |
| `lastNGames` | `string \| undefined` | Query, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
try {
  const response = await apiController.playerdashptreboundlogsGET();

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



