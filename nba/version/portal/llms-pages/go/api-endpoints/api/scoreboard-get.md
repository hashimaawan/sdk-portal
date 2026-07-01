# Scoreboard GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRlNjb3JlYm9hcmRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```go
ScoreboardGET(
    ctx context.Context,
    gameDate string,
    leagueID string,
    dayOffset string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameDate` | `string` | Query, Required | - |
| `leagueID` | `string` | Query, Required | - |
| `dayOffset` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

gameDate := "GameDate8"

leagueID := "LeagueID4"

dayOffset := "DayOffset6"

resp, err := aPIController.ScoreboardGET(ctx, gameDate, leagueID, dayOffset)
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



