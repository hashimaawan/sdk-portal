# Scoreboard GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlNjb3JlYm9hcmRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
ScoreboardGetAsync(
    string gameDate,
    string leagueId,
    string dayOffset)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameDate` | `string` | Query, Required | - |
| `leagueId` | `string` | Query, Required | - |
| `dayOffset` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string gameDate = "GameDate8";
string leagueId = "LeagueID4";
string dayOffset = "DayOffset6";
try
{
    await api.ScoreboardGetAsync(
        gameDate,
        leagueId,
        dayOffset
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



