# Playbyplay GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlBsYXlieXBsYXlfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
PlaybyplayGetAsync(
    string gameId,
    string startPeriod,
    string endPeriod)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameId` | `string` | Query, Required | - |
| `startPeriod` | `string` | Query, Required | - |
| `endPeriod` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string gameId = "GameID8";
string startPeriod = "StartPeriod4";
string endPeriod = "EndPeriod0";
try
{
    await api.PlaybyplayGetAsync(
        gameId,
        startPeriod,
        endPeriod
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



