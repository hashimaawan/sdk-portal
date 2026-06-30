# Get All Actions for a Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlJTI1MjBBY3Rpb25zJTJGR2V0JTI1MjBhbGwlMjUyMEFjdGlvbnMlMjUyMGZvciUyNTIwYSUyNTIwQ2VydGlmaWNhdGU

Returns all Action objects for a Certificate. You can sort the results by using the `sort` URI parameter, and filter them with the `status` parameter.

Only type `managed` Certificates can have Actions. For type `uploaded` Certificates the `actions` key will always contain an empty array.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_actions_for_a_certificate(self,
                                     id,
                                     sort=None,
                                     status=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Resource |
| `sort` | [`ParameterSortEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/parameter-sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`ParameterStatusEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/parameter-status.md) | Query, Optional | Can be used multiple times, the response will contain only Actions with specified statuses |


# Response Type

**200**: The `actions` key contains a list of Actions

[`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/actions-response.md)


# Example Usage

```python
id = 112

result = certificate_actions_controller.get_all_actions_for_a_certificate(id)
print(result)
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



