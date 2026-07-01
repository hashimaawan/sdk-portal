# Playbyplay GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRlBsYXlieXBsYXlfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> playbyplayGetAsync(
    final String gameId,
    final String startPeriod,
    final String endPeriod)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameId` | `String` | Query, Required | - |
| `startPeriod` | `String` | Query, Required | - |
| `endPeriod` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String gameId = "GameID8";
String startPeriod = "StartPeriod4";
String endPeriod = "EndPeriod0";

api.playbyplayGetAsync(gameId, startPeriod, endPeriod).thenAccept(result -> {
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



