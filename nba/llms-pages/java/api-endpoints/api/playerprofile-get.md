# Playerprofile GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/java/x-redirect/JTI0ZSUyRiUyRlBsYXllcnByb2ZpbGVfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> playerprofileGETAsync(
    final String leagueID,
    final String playerID,
    final String season,
    final String seasonType,
    final String graphStartSeason,
    final String graphEndSeason,
    final String graphStat)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `String` | Query, Required | - |
| `playerID` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `seasonType` | `String` | Query, Required | - |
| `graphStartSeason` | `String` | Query, Required | - |
| `graphEndSeason` | `String` | Query, Required | - |
| `graphStat` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String leagueID = "LeagueID4";
String playerID = "PlayerID6";
String season = "Season0";
String seasonType = "SeasonType8";
String graphStartSeason = "GraphStartSeason2";
String graphEndSeason = "GraphEndSeason6";
String graphStat = "GraphStat0";

aPIController.playerprofileGETAsync(leagueID, playerID, season, seasonType, graphStartSeason, graphEndSeason, graphStat).thenAccept(result -> {
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



