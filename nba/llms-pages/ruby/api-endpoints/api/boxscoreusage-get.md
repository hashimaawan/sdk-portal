# Boxscoreusage GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/ruby/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JldXNhZ2VfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ruby
def boxscoreusage_get(game_id: nil,
                      start_period: nil,
                      end_period: nil,
                      start_range: nil,
                      end_range: nil,
                      range_type: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `game_id` | `String` | Query, Optional | - |
| `start_period` | `String` | Query, Optional | - |
| `end_period` | `String` | Query, Optional | - |
| `start_range` | `String` | Query, Optional | - |
| `end_range` | `String` | Query, Optional | - |
| `range_type` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```ruby
client_controller.boxscoreusage_get
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



