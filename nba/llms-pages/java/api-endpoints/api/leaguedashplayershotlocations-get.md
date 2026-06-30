# Leaguedashplayershotlocations GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/java/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwbGF5ZXJzaG90bG9jYXRpb25zX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> leaguedashplayershotlocationsGETAsync(
    final String measureType,
    final String perMode,
    final String plusMinus,
    final String paceAdjust,
    final String rank,
    final String season,
    final String seasonType,
    final String outcome,
    final String location,
    final String month,
    final String seasonSegment,
    final String dateFrom,
    final String dateTo,
    final String opponentTeamID,
    final String vsConference,
    final String vsDivision,
    final String gameSegment,
    final String period,
    final String lastNGames,
    final String distanceRange,
    final String gameScope,
    final String playerExperience,
    final String playerPosition,
    final String starterBench)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `measureType` | `String` | Query, Required | - |
| `perMode` | `String` | Query, Required | - |
| `plusMinus` | `String` | Query, Required | - |
| `paceAdjust` | `String` | Query, Required | - |
| `rank` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `seasonType` | `String` | Query, Required | - |
| `outcome` | `String` | Query, Required | - |
| `location` | `String` | Query, Required | - |
| `month` | `String` | Query, Required | - |
| `seasonSegment` | `String` | Query, Required | - |
| `dateFrom` | `String` | Query, Required | - |
| `dateTo` | `String` | Query, Required | - |
| `opponentTeamID` | `String` | Query, Required | - |
| `vsConference` | `String` | Query, Required | - |
| `vsDivision` | `String` | Query, Required | - |
| `gameSegment` | `String` | Query, Required | - |
| `period` | `String` | Query, Required | - |
| `lastNGames` | `String` | Query, Required | - |
| `distanceRange` | `String` | Query, Required | - |
| `gameScope` | `String` | Query, Required | - |
| `playerExperience` | `String` | Query, Required | - |
| `playerPosition` | `String` | Query, Required | - |
| `starterBench` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String measureType = "MeasureType8";
String perMode = "PerMode6";
String plusMinus = "PlusMinus0";
String paceAdjust = "PaceAdjust2";
String rank = "Rank2";
String season = "Season0";
String seasonType = "SeasonType8";
String outcome = "Outcome4";
String location = "Location4";
String month = "Month0";
String seasonSegment = "SeasonSegment8";
String dateFrom = "DateFrom6";
String dateTo = "DateTo0";
String opponentTeamID = "OpponentTeamID6";
String vsConference = "VsConference6";
String vsDivision = "VsDivision6";
String gameSegment = "GameSegment6";
String period = "Period2";
String lastNGames = "LastNGames4";
String distanceRange = "DistanceRange6";
String gameScope = "GameScope0";
String playerExperience = "PlayerExperience4";
String playerPosition = "PlayerPosition8";
String starterBench = "StarterBench0";

aPIController.leaguedashplayershotlocationsGETAsync(measureType, perMode, plusMinus, paceAdjust, rank, season, seasonType, outcome, location, month, seasonSegment, dateFrom, dateTo, opponentTeamID, vsConference, vsDivision, gameSegment, period, lastNGames, distanceRange, gameScope, playerExperience, playerPosition, starterBench).thenAccept(result -> {
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



