# Get All Actions for a Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlJTI1MjBBY3Rpb25zJTJGR2V0JTI1MjBhbGwlMjUyMEFjdGlvbnMlMjUyMGZvciUyNTIwYSUyNTIwQ2VydGlmaWNhdGU

Returns all Action objects for a Certificate. You can sort the results by using the `sort` URI parameter, and filter them with the `status` parameter.

Only type `managed` Certificates can have Actions. For type `uploaded` Certificates the `actions` key will always contain an empty array.

:information_source: **Note** This endpoint does not require authentication.

```ts
async getAllActionsForACertificate(
  id: number,
  sort?: ParameterSort,
  status?: ParameterStatus,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ActionsResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Resource |
| `sort` | [`ParameterSort \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/parameter-sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`ParameterStatus \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/parameter-status.md) | Query, Optional | Can be used multiple times, the response will contain only Actions with specified statuses |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `actions` key contains a list of Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/actions-response.md).


# Example Usage

```ts
const id = 112;

try {
  const response = await certificateActionsApi.getAllActionsForACertificate(id);

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
      "command": "issue_certificate",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": "2021-01-30T23:57:00+00:00",
      "id": 14,
      "progress": 100,
      "resources": [
        {
          "id": 896,
          "type": "certificate"
        }
      ],
      "started": "2021-01-30T23:55:00+00:00",
      "status": "success"
    }
  ]
}
```



