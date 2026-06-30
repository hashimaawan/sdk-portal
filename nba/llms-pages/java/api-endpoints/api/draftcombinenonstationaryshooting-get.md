# Draftcombinenonstationaryshooting GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/java/x-redirect/JTI0ZSUyRiUyRkRyYWZ0Y29tYmluZW5vbnN0YXRpb25hcnlzaG9vdGluZ19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> draftcombinenonstationaryshootingGETAsync(
    final String leagueID,
    final String seasonYear)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `String` | Query, Required | - |
| `seasonYear` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String leagueID = "LeagueID4";
String seasonYear = "SeasonYear6";

aPIController.draftcombinenonstationaryshootingGETAsync(leagueID, seasonYear).thenAccept(result -> {
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



