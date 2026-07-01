# Boxscoreusagev 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JldXNhZ2V2Ml9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```csharp
Boxscoreusagev2GetAsync(
    string gameId,
    string startPeriod,
    string endPeriod,
    string startRange,
    string endRange,
    string rangeType)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameId` | `string` | Query, Required | - |
| `startPeriod` | `string` | Query, Required | - |
| `endPeriod` | `string` | Query, Required | - |
| `startRange` | `string` | Query, Required | - |
| `endRange` | `string` | Query, Required | - |
| `rangeType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string gameId = "GameID8";
string startPeriod = "StartPeriod4";
string endPeriod = "EndPeriod0";
string startRange = "StartRange0";
string endRange = "EndRange2";
string rangeType = "RangeType0";
try
{
    await api.Boxscoreusagev2GetAsync(
        gameId,
        startPeriod,
        endPeriod,
        startRange,
        endRange,
        rangeType
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



