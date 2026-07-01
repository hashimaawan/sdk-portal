# Commonplayoffseries GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkNvbW1vbnBsYXlvZmZzZXJpZXNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
CommonplayoffseriesGetAsync(
    string leagueId,
    string season)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string leagueId = "LeagueID4";
string season = "Season0";
try
{
    await api.CommonplayoffseriesGetAsync(
        leagueId,
        season
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



