# Get All Prices

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlByaWNpbmclMkZHZXQlMjUyMGFsbCUyNTIwcHJpY2Vz

Returns prices for all resources available on the platform. VAT and currency of the Project owner are used for calculations.

Both net and gross prices are included in the response.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<PricingResponse>> getAllPricesAsync()
```


# Response Type

**200**: The `pricing` key in the reply contains an pricing object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PricingResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/pricing-response.md).


# Example Usage

```java
pricingApi.getAllPricesAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



