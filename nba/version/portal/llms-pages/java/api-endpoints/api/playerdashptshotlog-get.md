# Playerdashptshotlog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHNob3Rsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> playerdashptshotlogGetAsync(
    final String leagueId,
    final String season,
    final String seasonType,
    final String playerId,
    final String teamId)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `String` | Query, Optional | - |
| `season` | `String` | Query, Optional | - |
| `seasonType` | `String` | Query, Optional | - |
| `playerId` | `String` | Query, Optional | - |
| `teamId` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
api.playerdashptshotlogGetAsync(null, null, null, null, null).thenAccept(result -> {
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



