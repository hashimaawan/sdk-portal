# Teamyearbyyearstats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRlRlYW15ZWFyYnl5ZWFyc3RhdHNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> teamyearbyyearstatsGetAsync(
    final String leagueId,
    final String seasonType,
    final String perMode,
    final String teamId)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `String` | Query, Required | - |
| `seasonType` | `String` | Query, Required | - |
| `perMode` | `String` | Query, Required | - |
| `teamId` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String leagueId = "LeagueID4";
String seasonType = "SeasonType8";
String perMode = "PerMode6";
String teamId = "TeamID8";

api.teamyearbyyearstatsGetAsync(leagueId, seasonType, perMode, teamId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
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



