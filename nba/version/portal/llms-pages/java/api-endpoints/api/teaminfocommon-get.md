# Teaminfocommon GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRlRlYW1pbmZvY29tbW9uX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> teaminfocommonGetAsync(
    final String season,
    final String teamId,
    final String leagueId,
    final String seasonType)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `String` | Query, Required | - |
| `teamId` | `String` | Query, Required | - |
| `leagueId` | `String` | Query, Required | - |
| `seasonType` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String season = "Season0";
String teamId = "TeamID8";
String leagueId = "LeagueID4";
String seasonType = "SeasonType8";

api.teaminfocommonGetAsync(season, teamId, leagueId, seasonType).thenAccept(result -> {
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



