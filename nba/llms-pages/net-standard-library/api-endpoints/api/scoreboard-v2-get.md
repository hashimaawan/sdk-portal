# Scoreboard V2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlNjb3JlYm9hcmRWMl9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```csharp
ScoreboardV2GETAsync(
    string gameDate,
    string leagueID,
    string dayOffset)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameDate` | `string` | Query, Required | - |
| `leagueID` | `string` | Query, Required | - |
| `dayOffset` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string gameDate = "GameDate8";
string leagueID = "LeagueID4";
string dayOffset = "DayOffset6";
try
{
    await aPIController.ScoreboardV2GETAsync(
        gameDate,
        leagueID,
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



