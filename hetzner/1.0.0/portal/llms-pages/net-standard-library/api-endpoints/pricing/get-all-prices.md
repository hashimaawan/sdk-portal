# Get All Prices

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlByaWNpbmclMkZHZXQlMjUyMGFsbCUyNTIwcHJpY2Vz

Returns prices for all resources available on the platform. VAT and currency of the Project owner are used for calculations.

Both net and gross prices are included in the response.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAllPricesAsync()
```


# Response Type

**200**: The `pricing` key in the reply contains an pricing object with this structure

[`Task<Models.PricingResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/pricing-response.md)


# Example Usage

```csharp
try
{
    PricingResponse result = await pricingController.GetAllPricesAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



