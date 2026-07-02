# Droplets Get Destroy Associated Resources Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfZ2V0X0Rlc3Ryb3lBc3NvY2lhdGVkUmVzb3VyY2VzU3RhdHVz

To check on the status of a request to destroy a Droplet with its associated
resources, send a GET request to the
`/v2/droplets/$DROPLET_ID/destroy_with_associated_resources/status` endpoint.

```ts
async dropletsGetDestroyAssociatedResourcesStatus(
  dropletId: number,
  requestOptions?: RequestOptions
): Promise<
ApiResponse<V2DropletsDestroyWithAssociatedResourcesStatusResponse>
>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletId` | `number` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object containing containing the status of a request to destroy a Droplet and its associated resources.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2DropletsDestroyWithAssociatedResourcesStatusResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-droplets-destroy-with-associated-resources-status-response.md).


# Example Usage

```ts
const dropletId = 3164444;

try {
  const response = await dropletsApi.dropletsGetDestroyAssociatedResourcesStatus(dropletId);

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
  "completed_at": "2020-04-01T18:11:49Z",
  "droplet": {
    "destroyed_at": "2020-04-01T18:11:49Z",
    "id": "187000742",
    "name": "ubuntu-s-1vcpu-1gb-nyc1-01"
  },
  "failures": 0,
  "resources": {
    "floating_ips": [
      {
        "destroyed_at": "2020-04-01T18:11:44Z",
        "id": "6186916",
        "name": "45.55.96.47"
      }
    ],
    "reserved_ips": [
      {
        "destroyed_at": "2020-04-01T18:11:44Z",
        "id": "6186916",
        "name": "45.55.96.47"
      }
    ],
    "snapshots": [
      {
        "destroyed_at": "2020-04-01T18:11:44Z",
        "id": "61486916",
        "name": "ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330"
      }
    ],
    "volume_snapshots": [
      {
        "destroyed_at": "2020-04-01T18:11:44Z",
        "id": "edb0478d-7436-11ea-86e6-0a58ac144b91",
        "name": "volume-nyc1-01-1585758983629"
      }
    ],
    "volumes": []
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



