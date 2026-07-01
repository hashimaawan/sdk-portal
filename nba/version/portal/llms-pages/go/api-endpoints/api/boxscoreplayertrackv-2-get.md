# Boxscoreplayertrackv 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlcGxheWVydHJhY2t2Ml9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```go
Boxscoreplayertrackv2Get(
    ctx context.Context,
    gameId string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameId` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

gameId := "GameID8"

resp, err := api.Boxscoreplayertrackv2Get(ctx, gameId)
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



