# Leaguedashplayerbiostats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwbGF5ZXJiaW9zdGF0c19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```csharp
LeaguedashplayerbiostatsGetAsync(
    string perMode,
    string leagueId,
    string season,
    string seasonType)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perMode` | `string` | Query, Required | - |
| `leagueId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string perMode = "PerMode6";
string leagueId = "LeagueID4";
string season = "Season0";
string seasonType = "SeasonType8";
try
{
    await api.LeaguedashplayerbiostatsGetAsync(
        perMode,
        leagueId,
        season,
        seasonType
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



