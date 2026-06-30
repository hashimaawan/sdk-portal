# Teamdashptpass GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlRlYW1kYXNocHRwYXNzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```csharp
TeamdashptpassGETAsync(
    string perMode,
    string season,
    string seasonType,
    string teamID,
    string outcome,
    string location,
    string month,
    string seasonSegment,
    string dateFrom,
    string dateTo,
    string opponentTeamID,
    string vsConference,
    string vsDivision,
    string lastNGames)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perMode` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `teamID` | `string` | Query, Required | - |
| `outcome` | `string` | Query, Required | - |
| `location` | `string` | Query, Required | - |
| `month` | `string` | Query, Required | - |
| `seasonSegment` | `string` | Query, Required | - |
| `dateFrom` | `string` | Query, Required | - |
| `dateTo` | `string` | Query, Required | - |
| `opponentTeamID` | `string` | Query, Required | - |
| `vsConference` | `string` | Query, Required | - |
| `vsDivision` | `string` | Query, Required | - |
| `lastNGames` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string perMode = "PerMode6";
string season = "Season0";
string seasonType = "SeasonType8";
string teamID = "TeamID8";
string outcome = "Outcome4";
string location = "Location4";
string month = "Month0";
string seasonSegment = "SeasonSegment8";
string dateFrom = "DateFrom6";
string dateTo = "DateTo0";
string opponentTeamID = "OpponentTeamID6";
string vsConference = "VsConference6";
string vsDivision = "VsDivision6";
string lastNGames = "LastNGames4";
try
{
    await aPIController.TeamdashptpassGETAsync(
        perMode,
        season,
        seasonType,
        teamID,
        outcome,
        location,
        month,
        seasonSegment,
        dateFrom,
        dateTo,
        opponentTeamID,
        vsConference,
        vsDivision,
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



