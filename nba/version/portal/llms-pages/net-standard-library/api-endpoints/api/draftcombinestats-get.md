# Draftcombinestats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkRyYWZ0Y29tYmluZXN0YXRzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```csharp
DraftcombinestatsGetAsync(
    string leagueId,
    string seasonYear)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `seasonYear` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string leagueId = "LeagueID4";
string seasonYear = "SeasonYear6";
try
{
    await api.DraftcombinestatsGetAsync(
        leagueId,
        seasonYear
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



