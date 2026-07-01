# Trip Stop by Trip Id GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRiUyRlRyaXBTdG9wQnlUcmlwSWRfR0VU

list stops for a trip identified by {trip_id}

```go
TripStopByTripIdGet(
    ctx context.Context,
    tripId string) (
    models.ApiResponse[[]models.Step],
    error)
```


# Authentication

This endpoint requires [furkot_auth_access_code](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/go/getting-started/quickstart/authorization.md) **OR** [furkot_auth_implicit](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tripId` | `string` | Template, Required | id of the trip |


# Requires scope

## furkot_auth_access_code

`read:trips`

## furkot_auth_implicit

`read:trips`


# Response Type

**200**: Successful response

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [[]models.Step](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/go/models/structures/step.md).


# Example Usage

```go
ctx := context.Background()

tripId := "trip_id2"

apiResponse, err := api.TripStopByTripIdGet(ctx, tripId)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



