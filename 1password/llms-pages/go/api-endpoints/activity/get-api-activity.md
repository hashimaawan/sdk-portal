# Get Api Activity

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0ZSUyRkFjdGl2aXR5JTJGR2V0QXBpQWN0aXZpdHk

```go
GetApiActivity(
    ctx context.Context,
    limit *int,
    offset *int) (
    models.ApiResponse[[]models.ApiRequest],
    error)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `*int` | Query, Optional | How many API Events should be retrieved in a single request.<br><br>**Default**: `50` |
| `offset` | `*int` | Query, Optional | How far into the collection of API Events should the response start<br><br>**Default**: `0` |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [[]models.ApiRequest](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/api-request.md).


# Example Usage

```go
ctx := context.Background()

limit := 10

offset := 50

apiResponse, err := activityApi.GetApiActivity(ctx, &limit, &offset)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.ErrorResponse:
            log.Fatalln("ErrorResponseException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/exceptions/error-response.md) |



