# Allstarballotpredictor GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/go/x-redirect/JTI0ZSUyRiUyRkFsbHN0YXJiYWxsb3RwcmVkaWN0b3JfR0VU

:information_source: **Note** This endpoint does not require authentication.

```go
AllstarballotpredictorGet(
    ctx context.Context,
    westPlayer1 string,
    westPlayer2 string,
    westPlayer3 string,
    westPlayer4 string,
    westPlayer5 string,
    eastPlayer1 string,
    eastPlayer2 string,
    eastPlayer3 string,
    eastPlayer4 string,
    eastPlayer5 string,
    pointCap *string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `westPlayer1` | `string` | Query, Required | - |
| `westPlayer2` | `string` | Query, Required | - |
| `westPlayer3` | `string` | Query, Required | - |
| `westPlayer4` | `string` | Query, Required | - |
| `westPlayer5` | `string` | Query, Required | - |
| `eastPlayer1` | `string` | Query, Required | - |
| `eastPlayer2` | `string` | Query, Required | - |
| `eastPlayer3` | `string` | Query, Required | - |
| `eastPlayer4` | `string` | Query, Required | - |
| `eastPlayer5` | `string` | Query, Required | - |
| `pointCap` | `*string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

westPlayer1 := "WestPlayer10"

westPlayer2 := "WestPlayer24"

westPlayer3 := "WestPlayer32"

westPlayer4 := "WestPlayer48"

westPlayer5 := "WestPlayer56"

eastPlayer1 := "EastPlayer18"

eastPlayer2 := "EastPlayer26"

eastPlayer3 := "EastPlayer32"

eastPlayer4 := "EastPlayer44"

eastPlayer5 := "EastPlayer54"

resp, err := api.AllstarballotpredictorGet(ctx, westPlayer1, westPlayer2, westPlayer3, westPlayer4, westPlayer5, eastPlayer1, eastPlayer2, eastPlayer3, eastPlayer4, eastPlayer5, nil)
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



