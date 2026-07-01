# Teaminfocommon GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlRlYW1pbmZvY29tbW9uX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```csharp
TeaminfocommonGetAsync(
    string season,
    string teamId,
    string leagueId,
    string seasonType)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `string` | Query, Required | - |
| `teamId` | `string` | Query, Required | - |
| `leagueId` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string season = "Season0";
string teamId = "TeamID8";
string leagueId = "LeagueID4";
string seasonType = "SeasonType8";
try
{
    await api.TeaminfocommonGetAsync(
        season,
        teamId,
        leagueId,
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



