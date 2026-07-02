# Droplet Actions List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkRyb3BsZXQlMjUyMEFjdGlvbnMlMkZkcm9wbGV0QWN0aW9uc19saXN0

To retrieve a list of all actions that have been executed for a Droplet, send
a GET request to `/v2/droplets/$DROPLET_ID/actions`.

The results will be returned as a JSON object with an `actions` key. This will
be set to an array filled with `action` objects containing the standard
`action` attributes.

```ts
async dropletActionsList(
  dropletId: number,
  perPage?: number,
  page?: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2DropletsActionsResponse1>>
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

**200**: A JSON object with an `actions` key.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2DropletsActionsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-droplets-actions-response-1.md).


# Example Usage

```ts
const dropletId = 3164444;

const perPage = 2;

const page = 1;

try {
  const response = await dropletActionsApi.dropletActionsList(
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
  "actions": [
    {
      "completed_at": "2020-07-20T19:37:45Z",
      "id": 982864273,
      "region": {
        "available": true,
        "features": [
          "private_networking",
          "backups",
          "ipv6",
          "metadata",
          "install_agent",
          "image_transfer"
        ],
        "name": "New York 3",
        "sizes": [
          "s-1vcpu-1gb",
          "s-1vcpu-2gb",
          "s-3vcpu-1gb",
          "s-2vcpu-2gb",
          "s-1vcpu-3gb",
          "s-2vcpu-4gb",
          "s-4vcpu-8gb",
          "m-1vcpu-8gb",
          "s-6vcpu-16gb",
          "s-8vcpu-32gb",
          "s-12vcpu-48gb"
        ],
        "slug": "nyc3"
      },
      "region_slug": "nyc3",
      "resource_id": 3164444,
      "resource_type": "droplet",
      "started_at": "2020-07-20T19:37:30Z",
      "status": "completed",
      "type": "create"
    }
  ],
  "links": {},
  "meta": {
    "total": 1
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



