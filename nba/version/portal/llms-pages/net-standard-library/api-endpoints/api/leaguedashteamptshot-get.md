# Leaguedashteamptshot GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2h0ZWFtcHRzaG90X0dFVA

:information_source: **Note** This endpoint does not require authentication.

```csharp
LeaguedashteamptshotGetAsync(
    string leagueId,
    string perMode,
    string season,
    string seasonType)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string leagueId = "LeagueID4";
string perMode = "PerMode6";
string season = "Season0";
string seasonType = "SeasonType8";
try
{
    await api.LeaguedashteamptshotGetAsync(
        leagueId,
        perMode,
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



