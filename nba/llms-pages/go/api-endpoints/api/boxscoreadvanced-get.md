# Boxscoreadvanced GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/go/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlYWR2YW5jZWRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```go
BoxscoreadvancedGET(
    ctx context.Context,
    gameID *string,
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
| `gameID` | `*string` | Query, Optional | - |
| `startPeriod` | `*string` | Query, Optional | - |
| `endPeriod` | `*string` | Query, Optional | - |
| `startRange` | `*string` | Query, Optional | - |
| `endRange` | `*string` | Query, Optional | - |
| `rangeType` | `*string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

resp, err := aPIController.BoxscoreadvancedGET(ctx, nil, nil, nil, nil, nil, nil)
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



