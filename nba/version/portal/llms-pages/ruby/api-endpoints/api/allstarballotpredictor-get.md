# Allstarballotpredictor GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkFsbHN0YXJiYWxsb3RwcmVkaWN0b3JfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ruby
def allstarballotpredictor_get(west_player1,
                               west_player2,
                               west_player3,
                               west_player4,
                               west_player5,
                               east_player1,
                               east_player2,
                               east_player3,
                               east_player4,
                               east_player5,
                               point_cap: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `west_player_1` | `String` | Query, Required | - |
| `west_player_2` | `String` | Query, Required | - |
| `west_player_3` | `String` | Query, Required | - |
| `west_player_4` | `String` | Query, Required | - |
| `west_player_5` | `String` | Query, Required | - |
| `east_player_1` | `String` | Query, Required | - |
| `east_player_2` | `String` | Query, Required | - |
| `east_player_3` | `String` | Query, Required | - |
| `east_player_4` | `String` | Query, Required | - |
| `east_player_5` | `String` | Query, Required | - |
| `point_cap` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
west_player1 = 'WestPlayer10'

west_player2 = 'WestPlayer24'

west_player3 = 'WestPlayer32'

west_player4 = 'WestPlayer48'

west_player5 = 'WestPlayer56'

east_player1 = 'EastPlayer18'

east_player2 = 'EastPlayer26'

east_player3 = 'EastPlayer32'

east_player4 = 'EastPlayer44'

east_player5 = 'EastPlayer54'

result = client_api.allstarballotpredictor_get(
  west_player1,
  west_player2,
  west_player3,
  west_player4,
  west_player5,
  east_player1,
  east_player2,
  east_player3,
  east_player4,
  east_player5
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



