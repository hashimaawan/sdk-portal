# Playerprofile GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlBsYXllcnByb2ZpbGVfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
PlayerprofileGETAsync(
    string leagueID,
    string playerID,
    string season,
    string seasonType,
    string graphStartSeason,
    string graphEndSeason,
    string graphStat)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `playerID` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `graphStartSeason` | `string` | Query, Required | - |
| `graphEndSeason` | `string` | Query, Required | - |
| `graphStat` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string leagueID = "LeagueID4";
string playerID = "PlayerID6";
string season = "Season0";
string seasonType = "SeasonType8";
string graphStartSeason = "GraphStartSeason2";
string graphEndSeason = "GraphEndSeason6";
string graphStat = "GraphStat0";
try
{
    await aPIController.PlayerprofileGETAsync(
        leagueID,
        playerID,
        season,
        seasonType,
        graphStartSeason,
        graphEndSeason,
        graphStat
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



