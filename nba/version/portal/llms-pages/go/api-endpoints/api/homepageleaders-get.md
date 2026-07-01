# Homepageleaders GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRkhvbWVwYWdlbGVhZGVyc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```go
HomepageleadersGet(
    ctx context.Context,
    statCategory string,
    leagueId string,
    season string,
    seasonType string,
    playerOrTeam string,
    playerScope string,
    gameScope string,
    game *string,
    player *string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statCategory` | `string` | Query, Required | - |
| `leagueId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `playerOrTeam` | `string` | Query, Required | - |
| `playerScope` | `string` | Query, Required | - |
| `gameScope` | `string` | Query, Required | - |
| `game` | `*string` | Query, Optional | - |
| `player` | `*string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

statCategory := "StatCategory6"

leagueId := "LeagueID4"

season := "Season0"

seasonType := "SeasonType8"

playerOrTeam := "PlayerOrTeam8"

playerScope := "PlayerScope2"

gameScope := "GameScope0"

resp, err := api.HomepageleadersGet(ctx, statCategory, leagueId, season, seasonType, playerOrTeam, playerScope, gameScope, nil, nil)
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



