# Playersvsplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/go/x-redirect/JTI0ZSUyRiUyRlBsYXllcnN2c3BsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```go
PlayersvsplayersGET(
    ctx context.Context,
    playerTeamID string,
    playerID1 string,
    playerID2 string,
    playerID3 string,
    playerID4 string,
    playerID5 string,
    vsTeamID string,
    vsPlayerID1 string,
    vsPlayerID2 string,
    vsPlayerID3 string,
    vsPlayerID4 string,
    vsPlayerID5 string,
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
| `playerTeamID` | `string` | Query, Required | - |
| `playerID1` | `string` | Query, Required | - |
| `playerID2` | `string` | Query, Required | - |
| `playerID3` | `string` | Query, Required | - |
| `playerID4` | `string` | Query, Required | - |
| `playerID5` | `string` | Query, Required | - |
| `vsTeamID` | `string` | Query, Required | - |
| `vsPlayerID1` | `string` | Query, Required | - |
| `vsPlayerID2` | `string` | Query, Required | - |
| `vsPlayerID3` | `string` | Query, Required | - |
| `vsPlayerID4` | `string` | Query, Required | - |
| `vsPlayerID5` | `string` | Query, Required | - |
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
| `opponentTeamID` | `string` | Query, Required | - |
| `vsConference` | `string` | Query, Required | - |
| `vsDivision` | `string` | Query, Required | - |
| `gameSegment` | `string` | Query, Required | - |
| `period` | `string` | Query, Required | - |
| `lastNGames` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

playerTeamID := "PlayerTeamID4"

playerID1 := "PlayerID18"

playerID2 := "PlayerID24"

playerID3 := "PlayerID32"

playerID4 := "PlayerID44"

playerID5 := "PlayerID54"

vsTeamID := "VsTeamID8"

vsPlayerID1 := "VsPlayerID12"

vsPlayerID2 := "VsPlayerID28"

vsPlayerID3 := "VsPlayerID38"

vsPlayerID4 := "VsPlayerID46"

vsPlayerID5 := "VsPlayerID56"

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

opponentTeamID := "OpponentTeamID6"

vsConference := "VsConference6"

vsDivision := "VsDivision6"

gameSegment := "GameSegment6"

period := "Period2"

lastNGames := "LastNGames4"

resp, err := aPIController.PlayersvsplayersGET(ctx, playerTeamID, playerID1, playerID2, playerID3, playerID4, playerID5, vsTeamID, vsPlayerID1, vsPlayerID2, vsPlayerID3, vsPlayerID4, vsPlayerID5, seasonType, measureType, perMode, plusMinus, paceAdjust, rank, season, outcome, location, month, seasonSegment, dateFrom, dateTo, opponentTeamID, vsConference, vsDivision, gameSegment, period, lastNGames)
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



