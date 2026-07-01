# Get All Actions for a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGR2V0JTI1MjBhbGwlMjUyMEFjdGlvbnMlMjUyMGZvciUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Returns all Action objects for a Load Balancer. You can sort the results by using the `sort` URI parameter, and filter them with the `status` parameter.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAllActionsForALoadBalancerAsync(
    int id,
    Models.ParameterSort? sort = null,
    Models.ParameterStatus? status = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `sort` | [`ParameterSort?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/parameter-sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`ParameterStatus?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/parameter-status.md) | Query, Optional | Can be used multiple times, the response will contain only Actions with specified statuses |


# Response Type

**200**: The `actions` key contains a list of Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ActionsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/actions-response.md).


# Example Usage

```csharp
int id = 112;
try
{
    ApiResponse<ActionsResponse> result = await loadBalancerActionsApi.GetAllActionsForALoadBalancerAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Example Response *(as JSON)*

```json
{
  "actions": [
    {
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
  ]
}
```



