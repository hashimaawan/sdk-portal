# Teamgamelog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlRlYW1nYW1lbG9nX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```csharp
TeamgamelogGetAsync(
    string teamId,
    string season,
    string seasonType)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `teamId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string teamId = "TeamID8";
string season = "Season0";
string seasonType = "SeasonType8";
try
{
    await api.TeamgamelogGetAsync(
        teamId,
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



