# Get an Action for a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGR2V0JTI1MjBhbiUyNTIwQWN0aW9uJTI1MjBmb3IlMjUyMGElMjUyMExvYWQlMjUyMEJhbGFuY2Vy

Returns a specific Action for a Load Balancer.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAnActionForALoadBalancerAsync(
    int id,
    int actionId)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `actionId` | `int` | Template, Required | ID of the Action |


# Response Type

**200**: The `action` key contains the Load Balancer Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action-response.md).


# Example Usage

```csharp
int id = 112;
int actionId = 224;
try
{
    ApiResponse<ActionResponse> result = await loadBalancerActionsApi.GetAnActionForALoadBalancerAsync(
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
    "command": "change_protection",
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
        "type": "load_balancer"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



