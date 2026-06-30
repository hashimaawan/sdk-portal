# Playbyplayv 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/java/x-redirect/JTI0ZSUyRiUyRlBsYXlieXBsYXl2Ml9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> playbyplayv2GETAsync(
    final String gameID,
    final String startPeriod,
    final String endPeriod)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameID` | `String` | Query, Required | - |
| `startPeriod` | `String` | Query, Required | - |
| `endPeriod` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String gameID = "GameID8";
String startPeriod = "StartPeriod4";
String endPeriod = "EndPeriod0";

aPIController.playbyplayv2GETAsync(gameID, startPeriod, endPeriod).thenAccept(result -> {
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



