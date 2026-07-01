# Playersvsplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRlBsYXllcnN2c3BsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> playersvsplayersGETAsync(
    final String playerTeamID,
    final String playerID1,
    final String playerID2,
    final String playerID3,
    final String playerID4,
    final String playerID5,
    final String vsTeamID,
    final String vsPlayerID1,
    final String vsPlayerID2,
    final String vsPlayerID3,
    final String vsPlayerID4,
    final String vsPlayerID5,
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
    final String opponentTeamID,
    final String vsConference,
    final String vsDivision,
    final String gameSegment,
    final String period,
    final String lastNGames)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playerTeamID` | `String` | Query, Required | - |
| `playerID1` | `String` | Query, Required | - |
| `playerID2` | `String` | Query, Required | - |
| `playerID3` | `String` | Query, Required | - |
| `playerID4` | `String` | Query, Required | - |
| `playerID5` | `String` | Query, Required | - |
| `vsTeamID` | `String` | Query, Required | - |
| `vsPlayerID1` | `String` | Query, Required | - |
| `vsPlayerID2` | `String` | Query, Required | - |
| `vsPlayerID3` | `String` | Query, Required | - |
| `vsPlayerID4` | `String` | Query, Required | - |
| `vsPlayerID5` | `String` | Query, Required | - |
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
| `opponentTeamID` | `String` | Query, Required | - |
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
String playerTeamID = "PlayerTeamID4";
String playerID1 = "PlayerID18";
String playerID2 = "PlayerID24";
String playerID3 = "PlayerID32";
String playerID4 = "PlayerID44";
String playerID5 = "PlayerID54";
String vsTeamID = "VsTeamID8";
String vsPlayerID1 = "VsPlayerID12";
String vsPlayerID2 = "VsPlayerID28";
String vsPlayerID3 = "VsPlayerID38";
String vsPlayerID4 = "VsPlayerID46";
String vsPlayerID5 = "VsPlayerID56";
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
String opponentTeamID = "OpponentTeamID6";
String vsConference = "VsConference6";
String vsDivision = "VsDivision6";
String gameSegment = "GameSegment6";
String period = "Period2";
String lastNGames = "LastNGames4";

aPIController.playersvsplayersGETAsync(playerTeamID, playerID1, playerID2, playerID3, playerID4, playerID5, vsTeamID, vsPlayerID1, vsPlayerID2, vsPlayerID3, vsPlayerID4, vsPlayerID5, seasonType, measureType, perMode, plusMinus, paceAdjust, rank, season, outcome, location, month, seasonSegment, dateFrom, dateTo, opponentTeamID, vsConference, vsDivision, gameSegment, period, lastNGames).thenAccept(result -> {
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



