# Teamyearbyyearstats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlRlYW15ZWFyYnl5ZWFyc3RhdHNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
TeamyearbyyearstatsGetAsync(
    string leagueId,
    string seasonType,
    string perMode,
    string teamId)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `teamId` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string leagueId = "LeagueID4";
string seasonType = "SeasonType8";
string perMode = "PerMode6";
string teamId = "TeamID8";
try
{
    await api.TeamyearbyyearstatsGetAsync(
        leagueId,
        seasonType,
        perMode,
        teamId
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



