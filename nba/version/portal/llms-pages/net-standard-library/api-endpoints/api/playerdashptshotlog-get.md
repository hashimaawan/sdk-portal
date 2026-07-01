# Playerdashptshotlog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHNob3Rsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
PlayerdashptshotlogGETAsync(
    string leagueID = null,
    string season = null,
    string seasonType = null,
    string playerID = null,
    string teamID = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Optional | - |
| `season` | `string` | Query, Optional | - |
| `seasonType` | `string` | Query, Optional | - |
| `playerID` | `string` | Query, Optional | - |
| `teamID` | `string` | Query, Optional | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
try
{
    await aPIController.PlayerdashptshotlogGETAsync();
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



