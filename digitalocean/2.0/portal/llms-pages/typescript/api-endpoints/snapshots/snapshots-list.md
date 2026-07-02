# Snapshots List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRlNuYXBzaG90cyUyRnNuYXBzaG90c19saXN0

To list all of the snapshots available on your account, send a GET request to
`/v2/snapshots`.

The response will be a JSON object with a key called `snapshots`. This will be
set to an array of `snapshot` objects, each of which will contain the standard
snapshot attributes.

### Filtering Results by Resource Type

It's possible to request filtered results by including certain query parameters.

#### List Droplet Snapshots

To retrieve only snapshots based on Droplets, include the `resource_type`
query parameter set to `droplet`. For example, `/v2/snapshots?resource_type=droplet`.

#### List Volume Snapshots

To retrieve only snapshots based on volumes, include the `resource_type`
query parameter set to `volume`. For example, `/v2/snapshots?resource_type=volume`.

```ts
async snapshotsList(
  perPage?: number,
  page?: number,
  resourceType?: ResourceType,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2SnapshotsResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perPage` | `number \| undefined` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `number \| undefined` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `resourceType` | [`ResourceType \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/resource-type.md) | Query, Optional | Used to filter snapshots by a resource type. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object with a key of `snapshots`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2SnapshotsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-snapshots-response.md).


# Example Usage

```ts
const perPage = 2;

const page = 1;

const resourceType = ResourceType.Droplet;

try {
  const response = await snapshotsApi.snapshotsList(
    perPage,
    page,
    resourceType
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
  "links": {},
  "meta": {
    "total": 2
  },
  "snapshots": [
    {
      "created_at": "2020-07-28T16:47:44Z",
      "id": "6372321",
      "min_disk_size": 25,
      "name": "web-01-1595954862243",
      "regions": [
        "nyc3",
        "sfo3"
      ],
      "resource_id": "200776916",
      "resource_type": "droplet",
      "size_gigabytes": 2.34,
      "tags": [
        "web",
        "env:prod"
      ]
    },
    {
      "created_at": "2019-09-28T23:14:30Z",
      "id": "fbe805e8-866b-11e6-96bf-000f53315a41",
      "min_disk_size": 2,
      "name": "pvc-01-1595954862243",
      "regions": [
        "nyc1"
      ],
      "resource_id": "89bcc42f-85cf-11e6-a004-000f53315871",
      "resource_type": "volume",
      "size_gigabytes": 0.1008,
      "tags": [
        "k8s"
      ]
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



