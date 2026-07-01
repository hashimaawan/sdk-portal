# Commonplayoffseries GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRkNvbW1vbnBsYXlvZmZzZXJpZXNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> commonplayoffseriesGETAsync(
    final String leagueID,
    final String season)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String leagueID = "LeagueID4";
String season = "Season0";

aPIController.commonplayoffseriesGETAsync(leagueID, season).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



