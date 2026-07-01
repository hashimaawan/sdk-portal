# Playerprofilev 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRlBsYXllcnByb2ZpbGV2Ml9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```csharp
Playerprofilev2GetAsync(
    string perMode,
    string playerId)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perMode` | `string` | Query, Required | - |
| `playerId` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string perMode = "PerMode6";
string playerId = "PlayerID6";
try
{
    await api.Playerprofilev2GetAsync(
        perMode,
        playerId
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



