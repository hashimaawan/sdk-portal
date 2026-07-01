# Remove from Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRkZpcmV3YWxsJTI1MjBBY3Rpb25zJTJGUmVtb3ZlJTI1MjBmcm9tJTI1MjBSZXNvdXJjZXM

Removes one Firewall from multiple resources.

Currently only Servers (and their public network interfaces) are supported.

#### Call specific error codes

| Code                                  | Description                                                            |
|---------------------------------------|------------------------------------------------------------------------|
| `firewall_already_removed`            | Firewall was already removed from the resource                         |
| `firewall_resource_not_found`         | The resource the Firewall should be attached to was not found          |
| `firewall_managed_by_label_selector`  | Firewall was applied via label selector and cannot be removed manually |

:information_source: **Note** This endpoint does not require authentication.

```ts
async removeFromResources(
  id: number,
  body?: RemoveFromResourcesRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ActionsResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Firewall |
| `body` | [`RemoveFromResourcesRequest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/remove-from-resources-request.md) | Body, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**201**: The `actions` key contains multiple `remove_firewall` Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/actions-response.md).


# Example Usage

```ts
const id = 112;

const body: RemoveFromResourcesRequest = {
  removeFrom: [
    {
      server: {
        id: 42,
      },
      type: Type7.Server,
    }
  ],
};

try {
  const response = await firewallActionsApi.removeFromResources(
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
  "actions": [
    {
      "command": "remove_firewall",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": "2016-01-30T23:56:00+00:00",
      "id": 14,
      "progress": 100,
      "resources": [
        {
          "id": 42,
          "type": "server"
        },
        {
          "id": 38,
          "type": "firewall"
        }
      ],
      "started": "2016-01-30T23:55:00+00:00",
      "status": "success"
    }
  ]
}
```



