# Playerdashptreboundlogs GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/java/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHJlYm91bmRsb2dzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> playerdashptreboundlogsGETAsync(
    final String season,
    final String seasonType,
    final String playerID,
    final String teamID,
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
| `season` | `String` | Query, Optional | - |
| `seasonType` | `String` | Query, Optional | - |
| `playerID` | `String` | Query, Optional | - |
| `teamID` | `String` | Query, Optional | - |
| `outcome` | `String` | Query, Optional | - |
| `location` | `String` | Query, Optional | - |
| `month` | `String` | Query, Optional | - |
| `seasonSegment` | `String` | Query, Optional | - |
| `dateFrom` | `String` | Query, Optional | - |
| `dateTo` | `String` | Query, Optional | - |
| `opponentTeamID` | `String` | Query, Optional | - |
| `vsConference` | `String` | Query, Optional | - |
| `vsDivision` | `String` | Query, Optional | - |
| `gameSegment` | `String` | Query, Optional | - |
| `period` | `String` | Query, Optional | - |
| `lastNGames` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
aPIController.playerdashptreboundlogsGETAsync(null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null).thenAccept(result -> {
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



