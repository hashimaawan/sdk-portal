# Playergamelog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/java/x-redirect/JTI0ZSUyRiUyRlBsYXllcmdhbWVsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> playergamelogGETAsync(
    final String playerID,
    final String season,
    final String seasonType)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playerID` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `seasonType` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String playerID = "PlayerID6";
String season = "Season0";
String seasonType = "SeasonType8";

aPIController.playergamelogGETAsync(playerID, season, seasonType).thenAccept(result -> {
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



