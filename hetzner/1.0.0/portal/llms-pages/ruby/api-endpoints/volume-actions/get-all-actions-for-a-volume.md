# Get All Actions for a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlZvbHVtZSUyNTIwQWN0aW9ucyUyRkdldCUyNTIwYWxsJTI1MjBBY3Rpb25zJTI1MjBmb3IlMjUyMGElMjUyMFZvbHVtZQ

Returns all Action objects for a Volume. You can `sort` the results by using the sort URI parameter, and filter them with the `status` parameter.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_all_actions_for_a_volume(id,
                                 sort: nil,
                                 status: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Volume |
| `sort` | [`ParameterSort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/parameter-sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`ParameterStatus`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/parameter-status.md) | Query, Optional | Can be used multiple times, the response will contain only Actions with specified statuses |


# Response Type

**200**: The `actions` key contains a list of Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/actions-response.md).


# Example Usage

```ruby
id = 112

result = volume_actions_api.get_all_actions_for_a_volume(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response *(as JSON)*

```json
{
  "actions": [
    {
      "command": "attach_volume",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": "2016-01-30T23:56:00+00:00",
      "id": 13,
      "progress": 100,
      "resources": [
        {
          "id": 42,
          "type": "server"
        },
        {
          "id": 13,
          "type": "volume"
        }
      ],
      "started": "2016-01-30T23:55:00+00:00",
      "status": "success"
    }
  ]
}
```



