# Shotchartdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```go
ShotchartdetailGet(
    ctx context.Context,
    seasonType string,
    teamId string,
    playerId string,
    gameId string,
    outcome string,
    location string,
    month string,
    seasonSegment string,
    dateFrom string,
    dateTo string,
    opponentTeamId string,
    vsConference string,
    vsDivision string,
    position string,
    rookieYear string,
    gameSegment string,
    period string,
    lastNGames string,
    contextMeasure string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `seasonType` | `string` | Query, Required | - |
| `teamId` | `string` | Query, Required | - |
| `playerId` | `string` | Query, Required | - |
| `gameId` | `string` | Query, Required | - |
| `outcome` | `string` | Query, Required | - |
| `location` | `string` | Query, Required | - |
| `month` | `string` | Query, Required | - |
| `seasonSegment` | `string` | Query, Required | - |
| `dateFrom` | `string` | Query, Required | - |
| `dateTo` | `string` | Query, Required | - |
| `opponentTeamId` | `string` | Query, Required | - |
| `vsConference` | `string` | Query, Required | - |
| `vsDivision` | `string` | Query, Required | - |
| `position` | `string` | Query, Required | - |
| `rookieYear` | `string` | Query, Required | - |
| `gameSegment` | `string` | Query, Required | - |
| `period` | `string` | Query, Required | - |
| `lastNGames` | `string` | Query, Required | - |
| `contextMeasure` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

seasonType := "SeasonType8"

teamId := "TeamID8"

playerId := "PlayerID6"

gameId := "GameID8"

outcome := "Outcome4"

location := "Location4"

month := "Month0"

seasonSegment := "SeasonSegment8"

dateFrom := "DateFrom6"

dateTo := "DateTo0"

opponentTeamId := "OpponentTeamID6"

vsConference := "VsConference6"

vsDivision := "VsDivision6"

position := "Position8"

rookieYear := "RookieYear8"

gameSegment := "GameSegment6"

period := "Period2"

lastNGames := "LastNGames4"

contextMeasure := "ContextMeasure2"

resp, err := api.ShotchartdetailGet(ctx, seasonType, teamId, playerId, gameId, outcome, location, month, seasonSegment, dateFrom, dateTo, opponentTeamId, vsConference, vsDivision, position, rookieYear, gameSegment, period, lastNGames, contextMeasure)
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



