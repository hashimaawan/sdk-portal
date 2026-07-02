# Cdn Create Endpoint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkNETiUyNTIwRW5kcG9pbnRzJTJGY2RuX2NyZWF0ZV9lbmRwb2ludA

To create a new CDN endpoint, send a POST request to `/v2/cdn/endpoints`. The
origin attribute must be set to the fully qualified domain name (FQDN) of a
DigitalOcean Space. Optionally, the TTL may be configured by setting the `ttl`
attribute.

A custom subdomain may be configured by specifying the `custom_domain` and
`certificate_id` attributes.

```ts
async cdnCreateEndpoint(
  body: Endpoint,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2CdnEndpointsResponse1>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Endpoint`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/endpoint.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**201**: The response will be a JSON object with an `endpoint` key. This will be set to an object containing the standard CDN endpoint attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2CdnEndpointsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-cdn-endpoints-response-1.md).


# Example Usage

```ts
const body: Endpoint = {
  origin: 'static-images.nyc3.digitaloceanspaces.com',
  ttl: Ttl.Enum3600,
};

try {
  const response = await cdnEndpointsApi.cdnCreateEndpoint(body);

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
  "endpoint": {
    "created_at": "2018-07-19T15:04:16Z",
    "endpoint": "static-images.nyc3.cdn.digitaloceanspaces.com",
    "id": "19f06b6a-3ace-4315-b086-499a0e521b76",
    "origin": "static-images.nyc3.digitaloceanspaces.com",
    "ttl": 3600
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



