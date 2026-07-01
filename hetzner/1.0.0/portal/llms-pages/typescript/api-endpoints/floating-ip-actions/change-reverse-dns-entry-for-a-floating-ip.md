# Change Reverse DNS Entry for a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRkNoYW5nZSUyNTIwcmV2ZXJzZSUyNTIwRE5TJTI1MjBlbnRyeSUyNTIwZm9yJTI1MjBhJTI1MjBGbG9hdGluZyUyNTIwSVA

Changes the hostname that will appear when getting the hostname belonging to this Floating IP.

:information_source: **Note** This endpoint does not require authentication.

```ts
async changeReverseDnsEntryForAFloatingIp(
  id: number,
  body?: ChangeDnsptrRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ActionResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Floating IP |
| `body` | [`ChangeDnsptrRequest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/change-dnsptr-request.md) | Body, Optional | Select the IP address for which to change the DNS entry by passing `ip`. For a Floating IP of type `ipv4` this must exactly match the IP address of the Floating IP. For a Floating IP of type `ipv6` this must be a single IP within the IPv6 /64 range that belongs to this Floating IP.<br><br>The target hostname is set by passing `dns_ptr`. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**201**: The `action` key contains the `change_dns_ptr` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action-response.md).


# Example Usage

```ts
const id = 112;

const body: ChangeDnsptrRequest = {
  dnsPtr: 'server02.example.com',
  ip: '1.2.3.4',
};

try {
  const response = await floatingIpActionsApi.changeReverseDnsEntryForAFloatingIp(
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
    "command": "change_dns_ptr",
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
        "type": "floating_ip"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



