# Playergamelog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRlBsYXllcmdhbWVsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> playergamelogGetAsync(
    final String playerId,
    final String season,
    final String seasonType)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playerId` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `seasonType` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String playerId = "PlayerID6";
String season = "Season0";
String seasonType = "SeasonType8";

api.playergamelogGetAsync(playerId, season, seasonType).thenAccept(result -> {
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



