# Databases List Firewall Rules

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19saXN0X2ZpcmV3YWxsX3J1bGVz

To list all of a database cluster's firewall rules (known as "trusted sources" in the control panel), send a GET request to `/v2/databases/$DATABASE_ID/firewall`.
The result will be a JSON object with a `rules` key.

```ts
async databasesListFirewallRules(
  databaseClusterUuid: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2DatabasesFirewallResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databaseClusterUuid` | `string` | Template, Required | A unique identifier for a database cluster. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object with a key of `rules`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2DatabasesFirewallResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-databases-firewall-response.md).


# Example Usage

```ts
const databaseClusterUuid = '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30';

try {
  const response = await databasesApi.databasesListFirewallRules(databaseClusterUuid);

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
  "rules": [
    {
      "cluster_uuid": "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
      "created_at": "2019-11-14T20:30:28Z",
      "type": "k8s",
      "uuid": "79f26d28-ea8a-41f2-8ad8-8cfcdd020095",
      "value": "ff2a6c52-5a44-4b63-b99c-0e98e7a63d61"
    },
    {
      "cluster_uuid": "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
      "created_at": "2019-11-14T20:30:28Z",
      "type": "ip_addr",
      "uuid": "adfe81a8-0fa1-4e2d-973f-06aa5af19b44",
      "value": "192.168.1.1"
    },
    {
      "cluster_uuid": "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
      "created_at": "2019-11-14T20:30:28Z",
      "type": "droplet",
      "uuid": "b9b42276-8295-4313-b40f-74173a7f46e6",
      "value": "163973392"
    },
    {
      "cluster_uuid": "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
      "created_at": "2019-11-14T20:30:28Z",
      "type": "tag",
      "uuid": "718d23e0-13d7-4129-8a00-47fb72ee0deb",
      "value": "backend"
    }
  ]
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



