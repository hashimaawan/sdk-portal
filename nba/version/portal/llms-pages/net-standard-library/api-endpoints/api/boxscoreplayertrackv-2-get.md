# Boxscoreplayertrackv 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlcGxheWVydHJhY2t2Ml9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```csharp
Boxscoreplayertrackv2GetAsync(
    string gameId)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameId` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string gameId = "GameID8";
try
{
    await api.Boxscoreplayertrackv2GetAsync(gameId);
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



