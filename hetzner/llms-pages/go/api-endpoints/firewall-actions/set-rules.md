# Set Rules

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0ZSUyRkZpcmV3YWxsJTI1MjBBY3Rpb25zJTJGU2V0JTI1MjBSdWxlcw

Sets the rules of a Firewall.

All existing rules will be overwritten. Pass an empty `rules` array to remove all rules.
The maximum amount of rules that can be defined is 50.

#### Call specific error codes

| Code                          | Description                                                   |
|-------------------------------|---------------------------------------------------------------|
| `firewall_resource_not_found` | The resource the Firewall should be attached to was not found |

:information_source: **Note** This endpoint does not require authentication.

```go
SetRules(
    ctx context.Context,
    id int,
    body *models.SetRulesRequest) (
    models.ApiResponse[models.ActionsResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Firewall |
| `body` | [`*models.SetRulesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/set-rules-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains one `set_firewall_rules` Action plus one `apply_firewall` Action per resource where the Firewall is active

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/actions-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.SetRulesRequest{
    Rules:                []models.Rule{
        models.Rule{
            Description:          models.NewOptional(models.ToPointer("Allow port 80")),
            Direction:            models.DirectionEnum_IN,
            Port:                 models.ToPointer("80"),
            Protocol:             models.ProtocolEnum_TCP,
            SourceIps:            []string{
                "28.239.13.1/32",
                "28.239.14.0/24",
                "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
            },
        },
    },
}

apiResponse, err := firewallActionsController.SetRules(ctx, id, &body)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Example Response *(as JSON)*

```json
{
  "actions": [
    {
      "command": "set_firewall_rules",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": "2016-01-30T23:56:00+00:00",
      "id": 13,
      "progress": 100,
      "resources": [
        {
          "id": 38,
          "type": "firewall"
        }
      ],
      "started": "2016-01-30T23:55:00+00:00",
      "status": "success"
    },
    {
      "command": "apply_firewall",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": "2016-01-30T23:56:00+00:00",
      "id": 14,
      "progress": 100,
      "resources": [
        {
          "id": 38,
          "type": "firewall"
        },
        {
          "id": 42,
          "type": "server"
        }
      ],
      "started": "2016-01-30T23:55:00+00:00",
      "status": "success"
    }
  ]
}
```



