# Apps List Regions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2xpc3RfcmVnaW9ucw

List all regions supported by App Platform.

```ts
async appsListRegions(
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2AppsRegionsResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object with key `regions`

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2AppsRegionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-apps-regions-response.md).


# Example Usage

```ts
try {
  const response = await appsApi.appsListRegions();

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
    if (error instanceof V21Clicks401Error) {
      console.log(error.result);
    }
  }
}
```


# Example Response *(as JSON)*

```json
{
  "regions": [
    {
      "continent": "Europe",
      "data_centers": [
        "ams3"
      ],
      "flag": "netherlands",
      "label": "Amsterdam",
      "slug": "ams"
    },
    {
      "continent": "North America",
      "data_centers": [
        "nyc1",
        "nyc3"
      ],
      "default": true,
      "flag": "usa",
      "label": "New York",
      "slug": "nyc"
    },
    {
      "continent": "Europe",
      "data_centers": [
        "fra1"
      ],
      "flag": "germany",
      "label": "Frankfurt",
      "slug": "fra"
    },
    {
      "continent": "North America",
      "data_centers": [
        "sfo3"
      ],
      "flag": "usa",
      "label": "San Francisco",
      "slug": "sfo"
    },
    {
      "continent": "Asia",
      "data_centers": [
        "sgp1"
      ],
      "flag": "singapore",
      "label": "Singapore",
      "slug": "sgp"
    },
    {
      "continent": "Asia",
      "data_centers": [
        "blr1"
      ],
      "flag": "india",
      "label": "Bangalore",
      "slug": "blr"
    },
    {
      "continent": "North America",
      "data_centers": [
        "tor1"
      ],
      "flag": "canada",
      "label": "Toronto",
      "slug": "tor"
    },
    {
      "continent": "Europe",
      "data_centers": [
        "lon1"
      ],
      "flag": "uk",
      "label": "London",
      "slug": "lon"
    }
  ]
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



