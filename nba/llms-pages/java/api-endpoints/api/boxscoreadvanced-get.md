# Boxscoreadvanced GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/java/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlYWR2YW5jZWRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> boxscoreadvancedGETAsync(
    final String gameID,
    final String startPeriod,
    final String endPeriod,
    final String startRange,
    final String endRange,
    final String rangeType)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameID` | `String` | Query, Optional | - |
| `startPeriod` | `String` | Query, Optional | - |
| `endPeriod` | `String` | Query, Optional | - |
| `startRange` | `String` | Query, Optional | - |
| `endRange` | `String` | Query, Optional | - |
| `rangeType` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
aPIController.boxscoreadvancedGETAsync(null, null, null, null, null, null).thenAccept(result -> {
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



