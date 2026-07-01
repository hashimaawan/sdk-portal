# Get All Prices

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlByaWNpbmclMkZHZXQlMjUyMGFsbCUyNTIwcHJpY2Vz

Returns prices for all resources available on the platform. VAT and currency of the Project owner are used for calculations.

Both net and gross prices are included in the response.

:information_source: **Note** This endpoint does not require authentication.

```go
GetAllPrices(
    ctx context.Context) (
    models.ApiResponse[models.PricingResponse],
    error)
```


# Response Type

**200**: The `pricing` key in the reply contains an pricing object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.PricingResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/pricing-response.md).


# Example Usage

```go
ctx := context.Background()

apiResponse, err := pricingApi.GetAllPrices(ctx)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



