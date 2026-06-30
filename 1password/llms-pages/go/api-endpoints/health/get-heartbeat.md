# Get Heartbeat

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0ZSUyRkhlYWx0aCUyRkdldEhlYXJ0YmVhdA

:information_source: **Note** This endpoint does not require authentication.

```go
GetHeartbeat(
    ctx context.Context) (
    models.ApiResponse[string],
    error)
```


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type string.


# Example Usage

```go
ctx := context.Background()

apiResponse, err := healthApi.GetHeartbeat(ctx)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



