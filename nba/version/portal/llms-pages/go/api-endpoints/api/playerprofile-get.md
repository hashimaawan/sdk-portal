# Playerprofile GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRlBsYXllcnByb2ZpbGVfR0VU

:information_source: **Note** This endpoint does not require authentication.

```go
PlayerprofileGet(
    ctx context.Context,
    leagueId string,
    playerId string,
    season string,
    seasonType string,
    graphStartSeason string,
    graphEndSeason string,
    graphStat string) (
    http.Response,
    error)
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


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

leagueId := "LeagueID4"

playerId := "PlayerID6"

season := "Season0"

seasonType := "SeasonType8"

graphStartSeason := "GraphStartSeason2"

graphEndSeason := "GraphEndSeason6"

graphStat := "GraphStat0"

resp, err := api.PlayerprofileGet(ctx, leagueId, playerId, season, seasonType, graphStartSeason, graphEndSeason, graphStat)
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



