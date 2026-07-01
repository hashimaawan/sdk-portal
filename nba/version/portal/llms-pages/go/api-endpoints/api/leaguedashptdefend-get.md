# Leaguedashptdefend GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwdGRlZmVuZF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```go
LeaguedashptdefendGet(
    ctx context.Context,
    leagueId string,
    perMode string,
    season string,
    seasonType string,
    defenseCategory string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `defenseCategory` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

leagueId := "LeagueID4"

perMode := "PerMode6"

season := "Season0"

seasonType := "SeasonType8"

defenseCategory := "DefenseCategory0"

resp, err := api.LeaguedashptdefendGet(ctx, leagueId, perMode, season, seasonType, defenseCategory)
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



