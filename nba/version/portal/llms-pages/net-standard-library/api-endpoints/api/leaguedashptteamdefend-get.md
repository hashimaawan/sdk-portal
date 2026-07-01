# Leaguedashptteamdefend GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwdHRlYW1kZWZlbmRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
LeaguedashptteamdefendGETAsync(
    string leagueID,
    string perMode,
    string season,
    string seasonType,
    string defenseCategory)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `defenseCategory` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string leagueID = "LeagueID4";
string perMode = "PerMode6";
string season = "Season0";
string seasonType = "SeasonType8";
string defenseCategory = "DefenseCategory0";
try
{
    await aPIController.LeaguedashptteamdefendGETAsync(
        leagueID,
        perMode,
        season,
        seasonType,
        defenseCategory
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



