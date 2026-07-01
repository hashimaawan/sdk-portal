# Homepageleaders GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/java/x-redirect/JTI0ZSUyRiUyRkhvbWVwYWdlbGVhZGVyc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> homepageleadersGetAsync(
    final String statCategory,
    final String leagueId,
    final String season,
    final String seasonType,
    final String playerOrTeam,
    final String playerScope,
    final String gameScope,
    final String game,
    final String player)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statCategory` | `String` | Query, Required | - |
| `leagueId` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `seasonType` | `String` | Query, Required | - |
| `playerOrTeam` | `String` | Query, Required | - |
| `playerScope` | `String` | Query, Required | - |
| `gameScope` | `String` | Query, Required | - |
| `game` | `String` | Query, Optional | - |
| `player` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```java
String statCategory = "StatCategory6";
String leagueId = "LeagueID4";
String season = "Season0";
String seasonType = "SeasonType8";
String playerOrTeam = "PlayerOrTeam8";
String playerScope = "PlayerScope2";
String gameScope = "GameScope0";

api.homepageleadersGetAsync(statCategory, leagueId, season, seasonType, playerOrTeam, playerScope, gameScope, null, null).thenAccept(result -> {
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



