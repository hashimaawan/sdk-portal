# Playersvsplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRlBsYXllcnN2c3BsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```go
PlayersvsplayersGet(
    ctx context.Context,
    playerTeamId string,
    playerId1 string,
    playerId2 string,
    playerId3 string,
    playerId4 string,
    playerId5 string,
    vsTeamId string,
    vsPlayerId1 string,
    vsPlayerId2 string,
    vsPlayerId3 string,
    vsPlayerId4 string,
    vsPlayerId5 string,
    seasonType string,
    measureType string,
    perMode string,
    plusMinus string,
    paceAdjust string,
    rank string,
    season string,
    outcome string,
    location string,
    month string,
    seasonSegment string,
    dateFrom string,
    dateTo string,
    opponentTeamId string,
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
| `playerTeamId` | `string` | Query, Required | - |
| `playerId1` | `string` | Query, Required | - |
| `playerId2` | `string` | Query, Required | - |
| `playerId3` | `string` | Query, Required | - |
| `playerId4` | `string` | Query, Required | - |
| `playerId5` | `string` | Query, Required | - |
| `vsTeamId` | `string` | Query, Required | - |
| `vsPlayerId1` | `string` | Query, Required | - |
| `vsPlayerId2` | `string` | Query, Required | - |
| `vsPlayerId3` | `string` | Query, Required | - |
| `vsPlayerId4` | `string` | Query, Required | - |
| `vsPlayerId5` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `measureType` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `plusMinus` | `string` | Query, Required | - |
| `paceAdjust` | `string` | Query, Required | - |
| `rank` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `outcome` | `string` | Query, Required | - |
| `location` | `string` | Query, Required | - |
| `month` | `string` | Query, Required | - |
| `seasonSegment` | `string` | Query, Required | - |
| `dateFrom` | `string` | Query, Required | - |
| `dateTo` | `string` | Query, Required | - |
| `opponentTeamId` | `string` | Query, Required | - |
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

playerTeamId := "PlayerTeamID4"

playerId1 := "PlayerID18"

playerId2 := "PlayerID24"

playerId3 := "PlayerID32"

playerId4 := "PlayerID44"

playerId5 := "PlayerID54"

vsTeamId := "VsTeamID8"

vsPlayerId1 := "VsPlayerID12"

vsPlayerId2 := "VsPlayerID28"

vsPlayerId3 := "VsPlayerID38"

vsPlayerId4 := "VsPlayerID46"

vsPlayerId5 := "VsPlayerID56"

seasonType := "SeasonType8"

measureType := "MeasureType8"

perMode := "PerMode6"

plusMinus := "PlusMinus0"

paceAdjust := "PaceAdjust2"

rank := "Rank2"

season := "Season0"

outcome := "Outcome4"

location := "Location4"

month := "Month0"

seasonSegment := "SeasonSegment8"

dateFrom := "DateFrom6"

dateTo := "DateTo0"

opponentTeamId := "OpponentTeamID6"

vsConference := "VsConference6"

vsDivision := "VsDivision6"

gameSegment := "GameSegment6"

period := "Period2"

lastNGames := "LastNGames4"

resp, err := api.PlayersvsplayersGet(ctx, playerTeamId, playerId1, playerId2, playerId3, playerId4, playerId5, vsTeamId, vsPlayerId1, vsPlayerId2, vsPlayerId3, vsPlayerId4, vsPlayerId5, seasonType, measureType, perMode, plusMinus, paceAdjust, rank, season, outcome, location, month, seasonSegment, dateFrom, dateTo, opponentTeamId, vsConference, vsDivision, gameSegment, period, lastNGames)
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



