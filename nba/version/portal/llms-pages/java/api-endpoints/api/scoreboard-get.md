# Scoreboard GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRlNjb3JlYm9hcmRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> scoreboardGetAsync(
    final String gameDate,
    final String leagueId,
    final String dayOffset)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameDate` | `String` | Query, Required | - |
| `leagueId` | `String` | Query, Required | - |
| `dayOffset` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String gameDate = "GameDate8";
String leagueId = "LeagueID4";
String dayOffset = "DayOffset6";

api.scoreboardGetAsync(gameDate, leagueId, dayOffset).thenAccept(result -> {
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



