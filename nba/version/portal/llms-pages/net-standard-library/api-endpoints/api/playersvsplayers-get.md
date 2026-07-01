# Playersvsplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlBsYXllcnN2c3BsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
PlayersvsplayersGetAsync(
    string playerTeamId,
    string playerId1,
    string playerId2,
    string playerId3,
    string playerId4,
    string playerId5,
    string vsTeamId,
    string vsPlayerId1,
    string vsPlayerId2,
    string vsPlayerId3,
    string vsPlayerId4,
    string vsPlayerId5,
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
    string opponentTeamId,
    string vsConference,
    string vsDivision,
    string gameSegment,
    string period,
    string lastNGames)
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

`Task`


# Example Usage

```csharp
string playerTeamId = "PlayerTeamID4";
string playerId1 = "PlayerID18";
string playerId2 = "PlayerID24";
string playerId3 = "PlayerID32";
string playerId4 = "PlayerID44";
string playerId5 = "PlayerID54";
string vsTeamId = "VsTeamID8";
string vsPlayerId1 = "VsPlayerID12";
string vsPlayerId2 = "VsPlayerID28";
string vsPlayerId3 = "VsPlayerID38";
string vsPlayerId4 = "VsPlayerID46";
string vsPlayerId5 = "VsPlayerID56";
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
string opponentTeamId = "OpponentTeamID6";
string vsConference = "VsConference6";
string vsDivision = "VsDivision6";
string gameSegment = "GameSegment6";
string period = "Period2";
string lastNGames = "LastNGames4";
try
{
    await api.PlayersvsplayersGetAsync(
        playerTeamId,
        playerId1,
        playerId2,
        playerId3,
        playerId4,
        playerId5,
        vsTeamId,
        vsPlayerId1,
        vsPlayerId2,
        vsPlayerId3,
        vsPlayerId4,
        vsPlayerId5,
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
        opponentTeamId,
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



