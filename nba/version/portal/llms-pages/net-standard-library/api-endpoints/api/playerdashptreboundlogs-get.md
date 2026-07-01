# Playerdashptreboundlogs GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHJlYm91bmRsb2dzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```csharp
PlayerdashptreboundlogsGetAsync(
    string season = null,
    string seasonType = null,
    string playerId = null,
    string teamId = null,
    string outcome = null,
    string location = null,
    string month = null,
    string seasonSegment = null,
    string dateFrom = null,
    string dateTo = null,
    string opponentTeamId = null,
    string vsConference = null,
    string vsDivision = null,
    string gameSegment = null,
    string period = null,
    string lastNGames = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `string` | Query, Optional | - |
| `seasonType` | `string` | Query, Optional | - |
| `playerId` | `string` | Query, Optional | - |
| `teamId` | `string` | Query, Optional | - |
| `outcome` | `string` | Query, Optional | - |
| `location` | `string` | Query, Optional | - |
| `month` | `string` | Query, Optional | - |
| `seasonSegment` | `string` | Query, Optional | - |
| `dateFrom` | `string` | Query, Optional | - |
| `dateTo` | `string` | Query, Optional | - |
| `opponentTeamId` | `string` | Query, Optional | - |
| `vsConference` | `string` | Query, Optional | - |
| `vsDivision` | `string` | Query, Optional | - |
| `gameSegment` | `string` | Query, Optional | - |
| `period` | `string` | Query, Optional | - |
| `lastNGames` | `string` | Query, Optional | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
try
{
    await api.PlayerdashptreboundlogsGetAsync();
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



