# Shotchartdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```csharp
ShotchartdetailGetAsync(
    string seasonType,
    string teamId,
    string playerId,
    string gameId,
    string outcome,
    string location,
    string month,
    string seasonSegment,
    string dateFrom,
    string dateTo,
    string opponentTeamId,
    string vsConference,
    string vsDivision,
    string position,
    string rookieYear,
    string gameSegment,
    string period,
    string lastNGames,
    string contextMeasure)
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

`Task`


# Example Usage

```csharp
string seasonType = "SeasonType8";
string teamId = "TeamID8";
string playerId = "PlayerID6";
string gameId = "GameID8";
string outcome = "Outcome4";
string location = "Location4";
string month = "Month0";
string seasonSegment = "SeasonSegment8";
string dateFrom = "DateFrom6";
string dateTo = "DateTo0";
string opponentTeamId = "OpponentTeamID6";
string vsConference = "VsConference6";
string vsDivision = "VsDivision6";
string position = "Position8";
string rookieYear = "RookieYear8";
string gameSegment = "GameSegment6";
string period = "Period2";
string lastNGames = "LastNGames4";
string contextMeasure = "ContextMeasure2";
try
{
    await api.ShotchartdetailGetAsync(
        seasonType,
        teamId,
        playerId,
        gameId,
        outcome,
        location,
        month,
        seasonSegment,
        dateFrom,
        dateTo,
        opponentTeamId,
        vsConference,
        vsDivision,
        position,
        rookieYear,
        gameSegment,
        period,
        lastNGames,
        contextMeasure
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



