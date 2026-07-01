# Attach an ISO to a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkF0dGFjaCUyNTIwYW4lMjUyMElTTyUyNTIwdG8lMjUyMGElMjUyMFNlcnZlcg

Attaches an ISO to a Server. The Server will immediately see it as a new disk. An already attached ISO will automatically be detached before the new ISO is attached.

Servers with attached ISOs have a modified boot order: They will try to boot from the ISO first before falling back to hard disk.

:information_source: **Note** This endpoint does not require authentication.

```ts
async attachAnIsoToAServer(
  id: number,
  body?: ServersActionsAttachIsoRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ActionResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Server |
| `body` | [`ServersActionsAttachIsoRequest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/servers-actions-attach-iso-request.md) | Body, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action-response.md).


# Example Usage

```ts
const id = 112;

const body: ServersActionsAttachIsoRequest = {
  iso: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
};

try {
  const response = await serverActionsApi.attachAnIsoToAServer(
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
    "command": "attach_iso",
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



