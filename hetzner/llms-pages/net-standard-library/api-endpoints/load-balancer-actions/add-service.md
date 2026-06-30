# Add Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQWRkJTI1MjBTZXJ2aWNl

Adds a service to a Load Balancer.

#### Call specific error codes

| Code                       | Description                                             |
|----------------------------|---------------------------------------------------------|
| `source_port_already_used` | The source port you are trying to add is already in use |

:information_source: **Note** This endpoint does not require authentication.

```csharp
AddServiceAsync(
    int id,
    Models.LoadBalancerService body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`LoadBalancerService`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/load-balancer-service.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `add_service` Action

[`Task<Models.ActionResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/action-response.md)


# Example Usage

```csharp
int id = 112;
LoadBalancerService body = new LoadBalancerService
{
    DestinationPort = 80,
    HealthCheck = new LoadBalancerServiceHealthCheck
    {
        Interval = 15,
        Port = 4711,
        Protocol = Protocol6Enum.Http,
        Retries = 3,
        Timeout = 10,
    },
    ListenPort = 443,
    Protocol = Protocol7Enum.Https,
    Proxyprotocol = false,
};

try
{
    ActionResponse result = await loadBalancerActionsController.AddServiceAsync(
        id,
        body
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
    "command": "add_service",
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



