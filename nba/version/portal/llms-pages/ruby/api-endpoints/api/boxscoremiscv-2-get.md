# Boxscoremiscv 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlbWlzY3YyX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```ruby
def boxscoremiscv2_get(game_id,
                       start_period,
                       end_period,
                       start_range,
                       end_range,
                       range_type)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `game_id` | `String` | Query, Required | - |
| `start_period` | `String` | Query, Required | - |
| `end_period` | `String` | Query, Required | - |
| `start_range` | `String` | Query, Required | - |
| `end_range` | `String` | Query, Required | - |
| `range_type` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
game_id = 'GameID8'

start_period = 'StartPeriod4'

end_period = 'EndPeriod0'

start_range = 'StartRange0'

end_range = 'EndRange2'

range_type = 'RangeType0'

result = client_api.boxscoremiscv2_get(
  game_id,
  start_period,
  end_period,
  start_range,
  end_range,
  range_type
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



