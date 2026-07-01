# Shotchartdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> shotchartdetailGetAsync(
    final String seasonType,
    final String teamId,
    final String playerId,
    final String gameId,
    final String outcome,
    final String location,
    final String month,
    final String seasonSegment,
    final String dateFrom,
    final String dateTo,
    final String opponentTeamId,
    final String vsConference,
    final String vsDivision,
    final String position,
    final String rookieYear,
    final String gameSegment,
    final String period,
    final String lastNGames,
    final String contextMeasure)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `seasonType` | `String` | Query, Required | - |
| `teamId` | `String` | Query, Required | - |
| `playerId` | `String` | Query, Required | - |
| `gameId` | `String` | Query, Required | - |
| `outcome` | `String` | Query, Required | - |
| `location` | `String` | Query, Required | - |
| `month` | `String` | Query, Required | - |
| `seasonSegment` | `String` | Query, Required | - |
| `dateFrom` | `String` | Query, Required | - |
| `dateTo` | `String` | Query, Required | - |
| `opponentTeamId` | `String` | Query, Required | - |
| `vsConference` | `String` | Query, Required | - |
| `vsDivision` | `String` | Query, Required | - |
| `position` | `String` | Query, Required | - |
| `rookieYear` | `String` | Query, Required | - |
| `gameSegment` | `String` | Query, Required | - |
| `period` | `String` | Query, Required | - |
| `lastNGames` | `String` | Query, Required | - |
| `contextMeasure` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String seasonType = "SeasonType8";
String teamId = "TeamID8";
String playerId = "PlayerID6";
String gameId = "GameID8";
String outcome = "Outcome4";
String location = "Location4";
String month = "Month0";
String seasonSegment = "SeasonSegment8";
String dateFrom = "DateFrom6";
String dateTo = "DateTo0";
String opponentTeamId = "OpponentTeamID6";
String vsConference = "VsConference6";
String vsDivision = "VsDivision6";
String position = "Position8";
String rookieYear = "RookieYear8";
String gameSegment = "GameSegment6";
String period = "Period2";
String lastNGames = "LastNGames4";
String contextMeasure = "ContextMeasure2";

api.shotchartdetailGetAsync(seasonType, teamId, playerId, gameId, outcome, location, month, seasonSegment, dateFrom, dateTo, opponentTeamId, vsConference, vsDivision, position, rookieYear, gameSegment, period, lastNGames, contextMeasure).thenAccept(result -> {
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



