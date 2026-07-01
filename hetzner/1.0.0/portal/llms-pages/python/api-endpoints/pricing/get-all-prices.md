# Get All Prices

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlByaWNpbmclMkZHZXQlMjUyMGFsbCUyNTIwcHJpY2Vz

Returns prices for all resources available on the platform. VAT and currency of the Project owner are used for calculations.

Both net and gross prices are included in the response.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_prices(self)
```


# Response Type

**200**: The `pricing` key in the reply contains an pricing object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`PricingResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/pricing-response.md).


# Example Usage

```python
result = pricing_api.get_all_prices()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



