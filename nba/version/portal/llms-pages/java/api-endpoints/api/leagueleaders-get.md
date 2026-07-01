# Leagueleaders GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWxlYWRlcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> leagueleadersGETAsync(
    final String leagueID,
    final String perMode,
    final String season,
    final String seasonType,
    final String scope,
    final String statCategory)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `String` | Query, Required | - |
| `perMode` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `seasonType` | `String` | Query, Required | - |
| `scope` | `String` | Query, Required | - |
| `statCategory` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String leagueID = "LeagueID4";
String perMode = "PerMode6";
String season = "Season0";
String seasonType = "SeasonType8";
String scope = "Scope0";

aPIController.leagueleadersGETAsync(leagueID, perMode, season, seasonType, scope, null).thenAccept(result -> {
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



