# Shotchartdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```csharp
ShotchartdetailGETAsync(
    string seasonType,
    string teamID,
    string playerID,
    string gameID,
    string outcome,
    string location,
    string month,
    string seasonSegment,
    string dateFrom,
    string dateTo,
    string opponentTeamID,
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
| `teamID` | `string` | Query, Required | - |
| `playerID` | `string` | Query, Required | - |
| `gameID` | `string` | Query, Required | - |
| `outcome` | `string` | Query, Required | - |
| `location` | `string` | Query, Required | - |
| `month` | `string` | Query, Required | - |
| `seasonSegment` | `string` | Query, Required | - |
| `dateFrom` | `string` | Query, Required | - |
| `dateTo` | `string` | Query, Required | - |
| `opponentTeamID` | `string` | Query, Required | - |
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
string teamID = "TeamID8";
string playerID = "PlayerID6";
string gameID = "GameID8";
string outcome = "Outcome4";
string location = "Location4";
string month = "Month0";
string seasonSegment = "SeasonSegment8";
string dateFrom = "DateFrom6";
string dateTo = "DateTo0";
string opponentTeamID = "OpponentTeamID6";
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
    await aPIController.ShotchartdetailGETAsync(
        seasonType,
        teamID,
        playerID,
        gameID,
        outcome,
        location,
        month,
        seasonSegment,
        dateFrom,
        dateTo,
        opponentTeamID,
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



