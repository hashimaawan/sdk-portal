# Playercompare GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRlBsYXllcmNvbXBhcmVfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> playercompareGetAsync(
    final String playerIdList,
    final String vsPlayerIdList,
    final String seasonType,
    final String measureType,
    final String perMode,
    final String plusMinus,
    final String paceAdjust,
    final String rank,
    final String season,
    final String outcome,
    final String location,
    final String month,
    final String seasonSegment,
    final String dateFrom,
    final String dateTo,
    final String opponentTeamId,
    final String vsConference,
    final String vsDivision,
    final String gameSegment,
    final String period,
    final String lastNGames)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playerIdList` | `String` | Query, Required | - |
| `vsPlayerIdList` | `String` | Query, Required | - |
| `seasonType` | `String` | Query, Required | - |
| `measureType` | `String` | Query, Required | - |
| `perMode` | `String` | Query, Required | - |
| `plusMinus` | `String` | Query, Required | - |
| `paceAdjust` | `String` | Query, Required | - |
| `rank` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `outcome` | `String` | Query, Required | - |
| `location` | `String` | Query, Required | - |
| `month` | `String` | Query, Required | - |
| `seasonSegment` | `String` | Query, Required | - |
| `dateFrom` | `String` | Query, Required | - |
| `dateTo` | `String` | Query, Required | - |
| `opponentTeamId` | `String` | Query, Required | - |
| `vsConference` | `String` | Query, Required | - |
| `vsDivision` | `String` | Query, Required | - |
| `gameSegment` | `String` | Query, Required | - |
| `period` | `String` | Query, Required | - |
| `lastNGames` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String playerIdList = "PlayerIDList4";
String vsPlayerIdList = "VsPlayerIDList2";
String seasonType = "SeasonType8";
String measureType = "MeasureType8";
String perMode = "PerMode6";
String plusMinus = "PlusMinus0";
String paceAdjust = "PaceAdjust2";
String rank = "Rank2";
String season = "Season0";
String outcome = "Outcome4";
String location = "Location4";
String month = "Month0";
String seasonSegment = "SeasonSegment8";
String dateFrom = "DateFrom6";
String dateTo = "DateTo0";
String opponentTeamId = "OpponentTeamID6";
String vsConference = "VsConference6";
String vsDivision = "VsDivision6";
String gameSegment = "GameSegment6";
String period = "Period2";
String lastNGames = "LastNGames4";

api.playercompareGetAsync(playerIdList, vsPlayerIdList, seasonType, measureType, perMode, plusMinus, paceAdjust, rank, season, outcome, location, month, seasonSegment, dateFrom, dateTo, opponentTeamId, vsConference, vsDivision, gameSegment, period, lastNGames).thenAccept(result -> {
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



