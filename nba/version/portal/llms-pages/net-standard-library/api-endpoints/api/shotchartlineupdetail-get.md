# Shotchartlineupdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGxpbmV1cGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```csharp
ShotchartlineupdetailGetAsync(
    string leagueId,
    string season,
    string seasonType,
    string teamId,
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
    string lastNGames,
    string gameId,
    string groupId,
    string contextMeasure,
    string contextFilter)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `teamId` | `string` | Query, Required | - |
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
| `gameId` | `string` | Query, Required | - |
| `groupId` | `string` | Query, Required | - |
| `contextMeasure` | `string` | Query, Required | - |
| `contextFilter` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string leagueId = "LeagueID4";
string season = "Season0";
string seasonType = "SeasonType8";
string teamId = "TeamID8";
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
string gameId = "GameID8";
string groupId = "GROUP_ID6";
string contextMeasure = "ContextMeasure2";
string contextFilter = "ContextFilter6";
try
{
    await api.ShotchartlineupdetailGetAsync(
        leagueId,
        season,
        seasonType,
        teamId,
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
        lastNGames,
        gameId,
        groupId,
        contextMeasure,
        contextFilter
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



