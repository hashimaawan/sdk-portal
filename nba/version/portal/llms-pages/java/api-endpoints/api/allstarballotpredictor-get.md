# Allstarballotpredictor GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRkFsbHN0YXJiYWxsb3RwcmVkaWN0b3JfR0VU

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> allstarballotpredictorGETAsync(
    final String westPlayer1,
    final String westPlayer2,
    final String westPlayer3,
    final String westPlayer4,
    final String westPlayer5,
    final String eastPlayer1,
    final String eastPlayer2,
    final String eastPlayer3,
    final String eastPlayer4,
    final String eastPlayer5,
    final String pointCap)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `westPlayer1` | `String` | Query, Required | - |
| `westPlayer2` | `String` | Query, Required | - |
| `westPlayer3` | `String` | Query, Required | - |
| `westPlayer4` | `String` | Query, Required | - |
| `westPlayer5` | `String` | Query, Required | - |
| `eastPlayer1` | `String` | Query, Required | - |
| `eastPlayer2` | `String` | Query, Required | - |
| `eastPlayer3` | `String` | Query, Required | - |
| `eastPlayer4` | `String` | Query, Required | - |
| `eastPlayer5` | `String` | Query, Required | - |
| `pointCap` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String westPlayer1 = "WestPlayer10";
String westPlayer2 = "WestPlayer24";
String westPlayer3 = "WestPlayer32";
String westPlayer4 = "WestPlayer48";
String westPlayer5 = "WestPlayer56";
String eastPlayer1 = "EastPlayer18";
String eastPlayer2 = "EastPlayer26";
String eastPlayer3 = "EastPlayer32";
String eastPlayer4 = "EastPlayer44";
String eastPlayer5 = "EastPlayer54";

aPIController.allstarballotpredictorGETAsync(westPlayer1, westPlayer2, westPlayer3, westPlayer4, westPlayer5, eastPlayer1, eastPlayer2, eastPlayer3, eastPlayer4, eastPlayer5, null).thenAccept(result -> {
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



