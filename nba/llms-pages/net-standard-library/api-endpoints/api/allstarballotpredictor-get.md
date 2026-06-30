# Allstarballotpredictor GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/net-standard-library/x-redirect/JTI0ZSUyRiUyRkFsbHN0YXJiYWxsb3RwcmVkaWN0b3JfR0VU

:information_source: **Note** This endpoint does not require authentication.

```csharp
AllstarballotpredictorGETAsync(
    string westPlayer1,
    string westPlayer2,
    string westPlayer3,
    string westPlayer4,
    string westPlayer5,
    string eastPlayer1,
    string eastPlayer2,
    string eastPlayer3,
    string eastPlayer4,
    string eastPlayer5,
    string pointCap = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `westPlayer1` | `string` | Query, Required | - |
| `westPlayer2` | `string` | Query, Required | - |
| `westPlayer3` | `string` | Query, Required | - |
| `westPlayer4` | `string` | Query, Required | - |
| `westPlayer5` | `string` | Query, Required | - |
| `eastPlayer1` | `string` | Query, Required | - |
| `eastPlayer2` | `string` | Query, Required | - |
| `eastPlayer3` | `string` | Query, Required | - |
| `eastPlayer4` | `string` | Query, Required | - |
| `eastPlayer5` | `string` | Query, Required | - |
| `pointCap` | `string` | Query, Optional | - |


# Response Type

**200**: 200 OK

`Task`


# Example Usage

```csharp
string westPlayer1 = "WestPlayer10";
string westPlayer2 = "WestPlayer24";
string westPlayer3 = "WestPlayer32";
string westPlayer4 = "WestPlayer48";
string westPlayer5 = "WestPlayer56";
string eastPlayer1 = "EastPlayer18";
string eastPlayer2 = "EastPlayer26";
string eastPlayer3 = "EastPlayer32";
string eastPlayer4 = "EastPlayer44";
string eastPlayer5 = "EastPlayer54";
try
{
    await aPIController.AllstarballotpredictorGETAsync(
        westPlayer1,
        westPlayer2,
        westPlayer3,
        westPlayer4,
        westPlayer5,
        eastPlayer1,
        eastPlayer2,
        eastPlayer3,
        eastPlayer4,
        eastPlayer5
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



