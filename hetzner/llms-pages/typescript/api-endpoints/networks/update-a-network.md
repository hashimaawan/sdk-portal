# Update a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGVXBkYXRlJTI1MjBhJTI1MjBOZXR3b3Jr

Updates the network properties.

Note that when updating labels, the network’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

Note: if the network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```ts
async updateANetwork(
  id: number,
  body?: UpdateNetworkRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<NetworksResponse1>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the network |
| `body` | [`UpdateNetworkRequest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/update-network-request.md) | Body, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `network` key contains the updated network

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`NetworksResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/networks-response-1.md).


# Example Usage

```ts
const id = 112;

const body: UpdateNetworkRequest = {
  name: 'new-name',
};

try {
  const response = await networksController.updateANetwork(
    id,
    body
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
  }
}
```


# Example Response *(as JSON)*

```json
{
  "network": {
    "created": "2016-01-30T23:50:00+00:00",
    "id": 4711,
    "ip_range": "10.0.0.0/16",
    "labels": {
      "labelkey": "value"
    },
    "load_balancers": [
      42
    ],
    "name": "new-name",
    "protection": {
      "delete": false
    },
    "routes": [
      {
        "destination": "10.100.1.0/24",
        "gateway": "10.0.1.1"
      }
    ],
    "servers": [
      42
    ],
    "subnets": [
      {
        "gateway": "10.0.0.1",
        "ip_range": "10.0.1.0/24",
        "network_zone": "eu-central",
        "type": "cloud"
      }
    ]
  }
}
```



