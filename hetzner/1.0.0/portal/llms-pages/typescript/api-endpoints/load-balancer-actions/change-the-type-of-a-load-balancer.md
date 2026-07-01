# Change the Type of a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjB0aGUlMjUyMFR5cGUlMjUyMG9mJTI1MjBhJTI1MjBMb2FkJTI1MjBCYWxhbmNlcg

Changes the type (Max Services, Max Targets and Max Connections) of a Load Balancer.

**Call specific error codes**

| Code                         | Description                                                     |
|------------------------------|-----------------------------------------------------------------|
| `invalid_load_balancer_type` | The Load Balancer type does not fit for the given Load Balancer |

:information_source: **Note** This endpoint does not require authentication.

```ts
async changeTheTypeOfALoadBalancer(
  id: number,
  body?: ChangeTypeRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ActionResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Load Balancer |
| `body` | [`ChangeTypeRequest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/change-type-request.md) | Body, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**201**: The `action` key contains the `change_load_balancer_type` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action-response.md).


# Example Usage

```ts
const id = 112;

const body: ChangeTypeRequest = {
  loadBalancerType: 'lb21',
};

try {
  const response = await loadBalancerActionsApi.changeTheTypeOfALoadBalancer(
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
  "action": {
    "command": "change_load_balancer_type",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



