# Boxscore GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```csharp
BoxscoreGETAsync(
    string gameID = null,
    string startPeriod = null,
    string endPeriod = null,
    string startRange = null,
    string endRange = null,
    string rangeType = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameID` | `string` | Query, Optional | - |
| `startPeriod` | `string` | Query, Optional | - |
| `endPeriod` | `string` | Query, Optional | - |
| `startRange` | `string` | Query, Optional | - |
| `endRange` | `string` | Query, Optional | - |
| `rangeType` | `string` | Query, Optional | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
try
{
    await aPIController.BoxscoreGETAsync();
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



