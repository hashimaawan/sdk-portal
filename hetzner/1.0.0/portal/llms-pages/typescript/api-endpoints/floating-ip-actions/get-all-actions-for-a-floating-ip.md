# Get All Actions for a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRkdldCUyNTIwYWxsJTI1MjBBY3Rpb25zJTI1MjBmb3IlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Returns all Action objects for a Floating IP. You can sort the results by using the `sort` URI parameter, and filter them with the `status` parameter.

:information_source: **Note** This endpoint does not require authentication.

```ts
async getAllActionsForAFloatingIp(
  id: number,
  sort?: ParameterSort,
  status?: ParameterStatus,
  requestOptions?: RequestOptions
): Promise<ApiResponse<FloatingIpsActionsResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Floating IP |
| `sort` | [`ParameterSort \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/parameter-sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`ParameterStatus \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/parameter-status.md) | Query, Optional | Can be used multiple times, the response will contain only Actions with specified statuses |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `actions` key contains a list of Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`FloatingIpsActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/floating-ips-actions-response.md).


# Example Usage

```ts
const id = 112;

try {
  const response = await floatingIpActionsApi.getAllActionsForAFloatingIp(id);

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
  "actions": [
    {
      "command": "assign_floating_ip",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": "2016-01-30T23:56:00+00:00",
      "id": 13,
      "progress": 100,
      "resources": [
        {
          "id": 4711,
          "type": "server"
        },
        {
          "id": 4712,
          "type": "floating_ip"
        }
      ],
      "started": "2016-01-30T23:55:00+00:00",
      "status": "success"
    }
  ]
}
```



