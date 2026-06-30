# Teamyearbyyearstats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/java/x-redirect/JTI0ZSUyRiUyRlRlYW15ZWFyYnl5ZWFyc3RhdHNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> teamyearbyyearstatsGETAsync(
    final String leagueID,
    final String seasonType,
    final String perMode,
    final String teamID)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `String` | Query, Required | - |
| `seasonType` | `String` | Query, Required | - |
| `perMode` | `String` | Query, Required | - |
| `teamID` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String leagueID = "LeagueID4";
String seasonType = "SeasonType8";
String perMode = "PerMode6";
String teamID = "TeamID8";

aPIController.teamyearbyyearstatsGETAsync(leagueID, seasonType, perMode, teamID).thenAccept(result -> {
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



