# Playerdashptshotlog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHNob3Rsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```go
PlayerdashptshotlogGet(
    ctx context.Context,
    leagueId *string,
    season *string,
    seasonType *string,
    playerId *string,
    teamId *string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `*string` | Query, Optional | - |
| `season` | `*string` | Query, Optional | - |
| `seasonType` | `*string` | Query, Optional | - |
| `playerId` | `*string` | Query, Optional | - |
| `teamId` | `*string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

resp, err := api.PlayerdashptshotlogGet(ctx, nil, nil, nil, nil, nil)
if err != nil {
    log.Fatalln(err)
} else {
    fmt.Println(resp.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiError` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiError` |



