# Video Status GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlZpZGVvU3RhdHVzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```csharp
VideoStatusGetAsync(
    string leagueId,
    string gameDate)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `gameDate` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string leagueId = "LeagueID4";
string gameDate = "GameDate8";
try
{
    await api.VideoStatusGetAsync(
        leagueId,
        gameDate
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



