# Disable the Public Interface of a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGRGlzYWJsZSUyNTIwdGhlJTI1MjBwdWJsaWMlMjUyMGludGVyZmFjZSUyNTIwb2YlMjUyMGElMjUyMExvYWQlMjUyMEJhbGFuY2Vy

Disable the public interface of a Load Balancer. The Load Balancer will be not accessible from the internet via its public IPs.

#### Call specific error codes

| Code                                      | Description                                                                    |
|-------------------------------------------|--------------------------------------------------------------------------------|
| `load_balancer_not_attached_to_network`   |  The Load Balancer is not attached to a network                                |
| `targets_without_use_private_ip`          | The Load Balancer has targets that use the public IP instead of the private IP |

:information_source: **Note** This endpoint does not require authentication.

```ts
async disableThePublicInterfaceOfALoadBalancer(
  id: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ActionResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Load Balancer |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**201**: The `action` key contains the `disable_public_interface` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action-response.md).


# Example Usage

```ts
const id = 112;

try {
  const response = await loadBalancerActionsController.disableThePublicInterfaceOfALoadBalancer(id);

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
    "command": "disable_public_interface",
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
      },
      {
        "id": 4711,
        "type": "network"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



