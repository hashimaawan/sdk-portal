# Boxscoremiscv 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/go/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlbWlzY3YyX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```go
Boxscoremiscv2GET(
    ctx context.Context,
    gameID string,
    startPeriod string,
    endPeriod string,
    startRange string,
    endRange string,
    rangeType string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameID` | `string` | Query, Required | - |
| `startPeriod` | `string` | Query, Required | - |
| `endPeriod` | `string` | Query, Required | - |
| `startRange` | `string` | Query, Required | - |
| `endRange` | `string` | Query, Required | - |
| `rangeType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

gameID := "GameID8"

startPeriod := "StartPeriod4"

endPeriod := "EndPeriod0"

startRange := "StartRange0"

endRange := "EndRange2"

rangeType := "RangeType0"

resp, err := aPIController.Boxscoremiscv2GET(ctx, gameID, startPeriod, endPeriod, startRange, endRange, rangeType)
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



