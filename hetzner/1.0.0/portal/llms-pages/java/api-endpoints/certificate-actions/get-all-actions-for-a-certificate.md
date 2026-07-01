# Get All Actions for a Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlJTI1MjBBY3Rpb25zJTJGR2V0JTI1MjBhbGwlMjUyMEFjdGlvbnMlMjUyMGZvciUyNTIwYSUyNTIwQ2VydGlmaWNhdGU

Returns all Action objects for a Certificate. You can sort the results by using the `sort` URI parameter, and filter them with the `status` parameter.

Only type `managed` Certificates can have Actions. For type `uploaded` Certificates the `actions` key will always contain an empty array.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<ActionsResponse>> getAllActionsForACertificateAsync(
    final int id,
    final ParameterSort sort,
    final ParameterStatus status)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Resource |
| `sort` | [`ParameterSort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/parameter-sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`ParameterStatus`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/parameter-status.md) | Query, Optional | Can be used multiple times, the response will contain only Actions with specified statuses |


# Response Type

**200**: The `actions` key contains a list of Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/actions-response.md).


# Example Usage

```java
int id = 112;

certificateActionsApi.getAllActionsForACertificateAsync(id, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
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



