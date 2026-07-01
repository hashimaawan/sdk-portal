# Playerdashboardbyshootingsplits GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hib2FyZGJ5c2hvb3RpbmdzcGxpdHNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```go
PlayerdashboardbyshootingsplitsGET(
    ctx context.Context,
    measureType string,
    perMode string,
    plusMinus string,
    paceAdjust string,
    rank string,
    season string,
    seasonType string,
    playerID string,
    outcome string,
    location string,
    month string,
    seasonSegment string,
    dateFrom string,
    dateTo string,
    opponentTeamID string,
    vsConference string,
    vsDivision string,
    gameSegment string,
    period string,
    lastNGames string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `measureType` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `plusMinus` | `string` | Query, Required | - |
| `paceAdjust` | `string` | Query, Required | - |
| `rank` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `playerID` | `string` | Query, Required | - |
| `outcome` | `string` | Query, Required | - |
| `location` | `string` | Query, Required | - |
| `month` | `string` | Query, Required | - |
| `seasonSegment` | `string` | Query, Required | - |
| `dateFrom` | `string` | Query, Required | - |
| `dateTo` | `string` | Query, Required | - |
| `opponentTeamID` | `string` | Query, Required | - |
| `vsConference` | `string` | Query, Required | - |
| `vsDivision` | `string` | Query, Required | - |
| `gameSegment` | `string` | Query, Required | - |
| `period` | `string` | Query, Required | - |
| `lastNGames` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

measureType := "MeasureType8"

perMode := "PerMode6"

plusMinus := "PlusMinus0"

paceAdjust := "PaceAdjust2"

rank := "Rank2"

season := "Season0"

seasonType := "SeasonType8"

playerID := "PlayerID6"

outcome := "Outcome4"

location := "Location4"

month := "Month0"

seasonSegment := "SeasonSegment8"

dateFrom := "DateFrom6"

dateTo := "DateTo0"

opponentTeamID := "OpponentTeamID6"

vsConference := "VsConference6"

vsDivision := "VsDivision6"

gameSegment := "GameSegment6"

period := "Period2"

lastNGames := "LastNGames4"

resp, err := aPIController.PlayerdashboardbyshootingsplitsGET(ctx, measureType, perMode, plusMinus, paceAdjust, rank, season, seasonType, playerID, outcome, location, month, seasonSegment, dateFrom, dateTo, opponentTeamID, vsConference, vsDivision, gameSegment, period, lastNGames)
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



