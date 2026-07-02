# Registry Get Options

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkNvbnRhaW5lciUyNTIwUmVnaXN0cnklMkZyZWdpc3RyeV9nZXRfb3B0aW9ucw

This endpoint serves to provide additional information as to which option values are available when creating a container registry.
There are multiple subscription tiers available for container registry. Each tier allows a different number of image repositories to be created in your registry, and has a different amount of storage and transfer included.
There are multiple regions available for container registry and controls where your data is stored.
To list the available options, send a GET request to `/v2/registry/options`.

```php
function registryGetOptions(): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Response Type

**200**: The response will be a JSON object with a key called `options` which contains a key called `subscription_tiers` listing the available tiers.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2RegistryOptionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-registry-options-response.md).


# Example Usage

```php
$containerRegistryApi = $client->getContainerRegistryApi();
$apiResponse = $containerRegistryApi->registryGetOptions();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2RegistryOptionsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "options": {
    "available_regions": [
      "nyc3",
      "sfo3",
      "ams3",
      "sgp1",
      "fra1"
    ],
    "subscription_tiers": [
      {
        "allow_storage_overage": false,
        "eligibility_reasons": [
          "OverRepositoryLimit"
        ],
        "eligible": false,
        "included_bandwidth_bytes": 524288000,
        "included_repositories": 1,
        "included_storage_bytes": 524288000,
        "monthly_price_in_cents": 0,
        "name": "Starter",
        "slug": "starter"
      },
      {
        "allow_storage_overage": true,
        "eligible": true,
        "included_bandwidth_bytes": 5368709120,
        "included_repositories": 5,
        "included_storage_bytes": 5368709120,
        "monthly_price_in_cents": 500,
        "name": "Basic",
        "slug": "basic"
      },
      {
        "allow_storage_overage": true,
        "eligible": true,
        "included_bandwidth_bytes": 107374182400,
        "included_repositories": 0,
        "included_storage_bytes": 107374182400,
        "monthly_price_in_cents": 2000,
        "name": "Professional",
        "slug": "professional"
      }
    ]
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



