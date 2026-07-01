# Enable Rescue Mode for a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkVuYWJsZSUyNTIwUmVzY3VlJTI1MjBNb2RlJTI1MjBmb3IlMjUyMGElMjUyMFNlcnZlcg

Enable the Hetzner Rescue System for this Server. The next time a Server with enabled rescue mode boots it will start a special minimal Linux distribution designed for repair and reinstall.

In case a Server cannot boot on its own you can use this to access a Server’s disks.

Rescue Mode is automatically disabled when you first boot into it or if you do not use it for 60 minutes.

Enabling rescue mode will not [reboot](https://docs.hetzner.cloud/#server-actions-soft-reboot-a-server) your Server — you will have to do this yourself.

:information_source: **Note** This endpoint does not require authentication.

```ts
async enableRescueModeForAServer(
  id: number,
  body?: ServersActionsEnableRescueRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ServersActionsEnableRescueResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Server |
| `body` | [`ServersActionsEnableRescueRequest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/servers-actions-enable-rescue-request.md) | Body, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**201**: The `root_password` key in the reply contains the root password that can be used to access the booted rescue system.

The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ServersActionsEnableRescueResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/servers-actions-enable-rescue-response.md).


# Example Usage

```ts
const id = 112;

const body: ServersActionsEnableRescueRequest = {
  sshKeys: [
    2323
  ],
};

try {
  const response = await serverActionsApi.enableRescueModeForAServer(
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
    "command": "enable_rescue",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": "2016-01-30T23:56:00+00:00",
    "id": 13,
    "progress": 100,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  },
  "root_password": "zCWbFhnu950dUTko5f40"
}
```



