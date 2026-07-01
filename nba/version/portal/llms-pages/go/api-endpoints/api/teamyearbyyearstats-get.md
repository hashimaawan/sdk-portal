# Teamyearbyyearstats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRlRlYW15ZWFyYnl5ZWFyc3RhdHNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```go
TeamyearbyyearstatsGet(
    ctx context.Context,
    leagueId string,
    seasonType string,
    perMode string,
    teamId string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `teamId` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

leagueId := "LeagueID4"

seasonType := "SeasonType8"

perMode := "PerMode6"

teamId := "TeamID8"

resp, err := api.TeamyearbyyearstatsGet(ctx, leagueId, seasonType, perMode, teamId)
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



