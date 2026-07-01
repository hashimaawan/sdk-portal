# Get an Action for a Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlJTI1MjBBY3Rpb25zJTJGR2V0JTI1MjBhbiUyNTIwQWN0aW9uJTI1MjBmb3IlMjUyMGElMjUyMENlcnRpZmljYXRl

Returns a specific Action for a Certificate. Only type `managed` Certificates have Actions.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAnActionForACertificateAsync(
    int id,
    int actionId)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Certificate |
| `actionId` | `int` | Template, Required | ID of the Action |


# Response Type

**200**: The `action` key contains the Certificate Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action-response.md).


# Example Usage

```csharp
int id = 112;
int actionId = 224;
try
{
    ApiResponse<ActionResponse> result = await certificateActionsApi.GetAnActionForACertificateAsync(
        id,
        actionId
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Example Response *(as JSON)*

```json
{
  "action": {
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
}
```



