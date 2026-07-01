# Update an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRlVwZGF0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Updates an SSH key. You can update an SSH key name and an SSH key labels.

Please note that when updating labels, the SSH key current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```ts
async updateAnSSHKey(
  id: string,
  body?: SshKeysRequest1,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SshKeysResponse1>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | ID of the SSH key |
| `body` | [`SshKeysRequest1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ssh-keys-request-1.md) | Body, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `ssh_key` key in the reply contains the modified SSH key object with the new description

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`SshKeysResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ssh-keys-response-1.md).


# Example Usage

```ts
const id = 'id0';

const body: SshKeysRequest1 = {
  labels: { 'labelkey': 'value' },
  name: 'My ssh key',
};

try {
  const response = await sSHKeysController.updateAnSSHKey(
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
  "ssh_key": {
    "created": "2016-01-30T23:50:00+00:00",
    "fingerprint": "b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f",
    "id": 2323,
    "labels": {
      "labelkey": "value"
    },
    "name": "My ssh key",
    "public_key": "ssh-rsa AAAjjk76kgf...Xt"
  }
}
```



