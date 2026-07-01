# Homepageleaders GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkhvbWVwYWdlbGVhZGVyc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```csharp
HomepageleadersGetAsync(
    string statCategory,
    string leagueId,
    string season,
    string seasonType,
    string playerOrTeam,
    string playerScope,
    string gameScope,
    string game = null,
    string player = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statCategory` | `string` | Query, Required | - |
| `leagueId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `playerOrTeam` | `string` | Query, Required | - |
| `playerScope` | `string` | Query, Required | - |
| `gameScope` | `string` | Query, Required | - |
| `game` | `string` | Query, Optional | - |
| `player` | `string` | Query, Optional | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string statCategory = "StatCategory6";
string leagueId = "LeagueID4";
string season = "Season0";
string seasonType = "SeasonType8";
string playerOrTeam = "PlayerOrTeam8";
string playerScope = "PlayerScope2";
string gameScope = "GameScope0";
try
{
    await api.HomepageleadersGetAsync(
        statCategory,
        leagueId,
        season,
        seasonType,
        playerOrTeam,
        playerScope,
        gameScope
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



