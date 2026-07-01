# Boxscorefourfactors GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlZm91cmZhY3RvcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```go
BoxscorefourfactorsGet(
    ctx context.Context,
    gameId *string,
    startPeriod *string,
    endPeriod *string,
    startRange *string,
    endRange *string,
    rangeType *string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameId` | `*string` | Query, Optional | - |
| `startPeriod` | `*string` | Query, Optional | - |
| `endPeriod` | `*string` | Query, Optional | - |
| `startRange` | `*string` | Query, Optional | - |
| `endRange` | `*string` | Query, Optional | - |
| `rangeType` | `*string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

resp, err := api.BoxscorefourfactorsGet(ctx, nil, nil, nil, nil, nil, nil)
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



