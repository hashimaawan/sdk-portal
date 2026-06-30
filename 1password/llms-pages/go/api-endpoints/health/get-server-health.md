# Get Server Health

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0ZSUyRkhlYWx0aCUyRkdldFNlcnZlckhlYWx0aA

:information_source: **Note** This endpoint does not require authentication.

```go
GetServerHealth(
    ctx context.Context) (
    models.ApiResponse[models.HealthResponse],
    error)
```


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.HealthResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/health-response.md).


# Example Usage

```go
ctx := context.Background()

apiResponse, err := healthApi.GetServerHealth(ctx)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Example Response *(as JSON)*

```json
{
  "dependencies": [
    {
      "service": "sync",
      "status": "TOKEN_NEEDED"
    },
    {
      "message": "Connected to./1password.sqlite",
      "service": "sqlite",
      "status": "ACTIVE"
    }
  ],
  "name": "1Password Connect API",
  "version": "1.2.1"
}
```



