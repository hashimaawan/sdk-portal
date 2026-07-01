# Teaminfocommon GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRlRlYW1pbmZvY29tbW9uX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```go
TeaminfocommonGet(
    ctx context.Context,
    season string,
    teamId string,
    leagueId string,
    seasonType string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `string` | Query, Required | - |
| `teamId` | `string` | Query, Required | - |
| `leagueId` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

season := "Season0"

teamId := "TeamID8"

leagueId := "LeagueID4"

seasonType := "SeasonType8"

resp, err := api.TeaminfocommonGet(ctx, season, teamId, leagueId, seasonType)
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



