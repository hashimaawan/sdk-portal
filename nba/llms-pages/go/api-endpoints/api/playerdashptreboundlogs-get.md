# Playerdashptreboundlogs GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/go/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHJlYm91bmRsb2dzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```go
PlayerdashptreboundlogsGET(
    ctx context.Context,
    season *string,
    seasonType *string,
    playerID *string,
    teamID *string,
    outcome *string,
    location *string,
    month *string,
    seasonSegment *string,
    dateFrom *string,
    dateTo *string,
    opponentTeamID *string,
    vsConference *string,
    vsDivision *string,
    gameSegment *string,
    period *string,
    lastNGames *string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `*string` | Query, Optional | - |
| `seasonType` | `*string` | Query, Optional | - |
| `playerID` | `*string` | Query, Optional | - |
| `teamID` | `*string` | Query, Optional | - |
| `outcome` | `*string` | Query, Optional | - |
| `location` | `*string` | Query, Optional | - |
| `month` | `*string` | Query, Optional | - |
| `seasonSegment` | `*string` | Query, Optional | - |
| `dateFrom` | `*string` | Query, Optional | - |
| `dateTo` | `*string` | Query, Optional | - |
| `opponentTeamID` | `*string` | Query, Optional | - |
| `vsConference` | `*string` | Query, Optional | - |
| `vsDivision` | `*string` | Query, Optional | - |
| `gameSegment` | `*string` | Query, Optional | - |
| `period` | `*string` | Query, Optional | - |
| `lastNGames` | `*string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

resp, err := aPIController.PlayerdashptreboundlogsGET(ctx, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil, nil)
if err != nil {
    log.Fatalln(err)
} else {
    fmt.Println(resp.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiError` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiError` |



