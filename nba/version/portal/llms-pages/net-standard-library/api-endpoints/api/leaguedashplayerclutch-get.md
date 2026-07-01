# Leaguedashplayerclutch GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwbGF5ZXJjbHV0Y2hfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
LeaguedashplayerclutchGetAsync(
    string clutchTime,
    string aheadBehind,
    string pointDiff,
    string gameScope,
    string playerExperience,
    string playerPosition,
    string starterBench,
    string measureType,
    string perMode,
    string plusMinus,
    string paceAdjust,
    string rank,
    string season,
    string seasonType,
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
| `clutchTime` | `string` | Query, Required | - |
| `aheadBehind` | `string` | Query, Required | - |
| `pointDiff` | `string` | Query, Required | - |
| `gameScope` | `string` | Query, Required | - |
| `playerExperience` | `string` | Query, Required | - |
| `playerPosition` | `string` | Query, Required | - |
| `starterBench` | `string` | Query, Required | - |
| `measureType` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `plusMinus` | `string` | Query, Required | - |
| `paceAdjust` | `string` | Query, Required | - |
| `rank` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
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
string clutchTime = "ClutchTime4";
string aheadBehind = "AheadBehind8";
string pointDiff = "PointDiff6";
string gameScope = "GameScope0";
string playerExperience = "PlayerExperience4";
string playerPosition = "PlayerPosition8";
string starterBench = "StarterBench0";
string measureType = "MeasureType8";
string perMode = "PerMode6";
string plusMinus = "PlusMinus0";
string paceAdjust = "PaceAdjust2";
string rank = "Rank2";
string season = "Season0";
string seasonType = "SeasonType8";
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
    await api.LeaguedashplayerclutchGetAsync(
        clutchTime,
        aheadBehind,
        pointDiff,
        gameScope,
        playerExperience,
        playerPosition,
        starterBench,
        measureType,
        perMode,
        plusMinus,
        paceAdjust,
        rank,
        season,
        seasonType,
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



