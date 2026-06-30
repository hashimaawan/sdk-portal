# Commonallplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkNvbW1vbmFsbHBsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
CommonallplayersGETAsync(
    string leagueID,
    string season,
    string isOnlyCurrentSeason)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `isOnlyCurrentSeason` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string leagueID = "LeagueID4";
string season = "Season0";
string isOnlyCurrentSeason = "IsOnlyCurrentSeason6";
try
{
    await aPIController.CommonallplayersGETAsync(
        leagueID,
        season,
        isOnlyCurrentSeason
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



