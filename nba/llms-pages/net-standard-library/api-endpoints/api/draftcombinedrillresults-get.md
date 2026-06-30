# Draftcombinedrillresults GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkRyYWZ0Y29tYmluZWRyaWxscmVzdWx0c19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```csharp
DraftcombinedrillresultsGETAsync(
    string leagueID,
    string seasonYear)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `seasonYear` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string leagueID = "LeagueID4";
string seasonYear = "SeasonYear6";
try
{
    await aPIController.DraftcombinedrillresultsGETAsync(
        leagueID,
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



