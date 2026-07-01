# Playersvsplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlBsYXllcnN2c3BsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
PlayersvsplayersGETAsync(
    string playerTeamID,
    string playerID1,
    string playerID2,
    string playerID3,
    string playerID4,
    string playerID5,
    string vsTeamID,
    string vsPlayerID1,
    string vsPlayerID2,
    string vsPlayerID3,
    string vsPlayerID4,
    string vsPlayerID5,
    string seasonType,
    string measureType,
    string perMode,
    string plusMinus,
    string paceAdjust,
    string rank,
    string season,
    string outcome,
    string location,
    string month,
    string seasonSegment,
    string dateFrom,
    string dateTo,
    string opponentTeamID,
    string vsConference,
    string vsDivision,
    string gameSegment,
    string period,
    string lastNGames)
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

`Task`


# Example Usage

```csharp
string playerTeamID = "PlayerTeamID4";
string playerID1 = "PlayerID18";
string playerID2 = "PlayerID24";
string playerID3 = "PlayerID32";
string playerID4 = "PlayerID44";
string playerID5 = "PlayerID54";
string vsTeamID = "VsTeamID8";
string vsPlayerID1 = "VsPlayerID12";
string vsPlayerID2 = "VsPlayerID28";
string vsPlayerID3 = "VsPlayerID38";
string vsPlayerID4 = "VsPlayerID46";
string vsPlayerID5 = "VsPlayerID56";
string seasonType = "SeasonType8";
string measureType = "MeasureType8";
string perMode = "PerMode6";
string plusMinus = "PlusMinus0";
string paceAdjust = "PaceAdjust2";
string rank = "Rank2";
string season = "Season0";
string outcome = "Outcome4";
string location = "Location4";
string month = "Month0";
string seasonSegment = "SeasonSegment8";
string dateFrom = "DateFrom6";
string dateTo = "DateTo0";
string opponentTeamID = "OpponentTeamID6";
string vsConference = "VsConference6";
string vsDivision = "VsDivision6";
string gameSegment = "GameSegment6";
string period = "Period2";
string lastNGames = "LastNGames4";
try
{
    await aPIController.PlayersvsplayersGETAsync(
        playerTeamID,
        playerID1,
        playerID2,
        playerID3,
        playerID4,
        playerID5,
        vsTeamID,
        vsPlayerID1,
        vsPlayerID2,
        vsPlayerID3,
        vsPlayerID4,
        vsPlayerID5,
        seasonType,
        measureType,
        perMode,
        plusMinus,
        paceAdjust,
        rank,
        season,
        outcome,
        location,
        month,
        seasonSegment,
        dateFrom,
        dateTo,
        opponentTeamID,
        vsConference,
        vsDivision,
        gameSegment,
        period,
        lastNGames
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



