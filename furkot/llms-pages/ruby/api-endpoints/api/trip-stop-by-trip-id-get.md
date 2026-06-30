# Trip Stop by Trip Id GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/ruby/x-redirect/JTI0ZSUyRiUyRlRyaXBTdG9wQnlUcmlwSWRfR0VU

list stops for a trip identified by {trip_id}

```ruby
def trip_stop_by_trip_id_get(trip_id)
```


# Authentication

This endpoint requires [furkot_auth_access_code](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/ruby/getting-started/authorization.md) **OR** [furkot_auth_implicit](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/ruby/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `trip_id` | `String` | Template, Required | id of the trip |


# Requires scope

## furkot_auth_access_code

`read:trips`

## furkot_auth_implicit

`read:trips`


# Response Type

**200**: Successful response

[`Array[Step]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/ruby/models/structures/step.md)


# Example Usage

```ruby
trip_id = 'trip_id2'

result = client_controller.trip_stop_by_trip_id_get(trip_id)
puts result
```



