# Droplets List Kernels

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfbGlzdF9rZXJuZWxz

To retrieve a list of all kernels available to a Droplet, send a GET request
to `/v2/droplets/$DROPLET_ID/kernels`

The response will be a JSON object that has a key called `kernels`. This will
be set to an array of `kernel` objects, each of which contain the standard
`kernel` attributes.

```ts
async dropletsListKernels(
  dropletId: number,
  perPage?: number,
  page?: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2DropletsKernelsResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletId` | `number` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |
| `perPage` | `number \| undefined` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `number \| undefined` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object that has a key called `kernels`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2DropletsKernelsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-droplets-kernels-response.md).


# Example Usage

```ts
const dropletId = 3164444;

const perPage = 2;

const page = 1;

try {
  const response = await dropletsApi.dropletsListKernels(
    dropletId,
    perPage,
    page
  );

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
  "kernels": [
    {
      "id": 7515,
      "name": "DigitalOcean GrubLoader v0.2 (20160714)",
      "version": "2016.07.13-DigitalOcean_loader_Ubuntu"
    }
  ],
  "links": {
    "pages": {
      "last": "https://api.digitalocean.com/v2/droplets/3164444/kernels?page=171&per_page=1",
      "next": "https://api.digitalocean.com/v2/droplets/3164444/kernels?page=2&per_page=1"
    }
  },
  "meta": {
    "total": 171
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



