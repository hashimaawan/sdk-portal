# Trip Stop by Trip Id GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlRyaXBTdG9wQnlUcmlwSWRfR0VU

list stops for a trip identified by {trip_id}

```ruby
def trip_stop_by_trip_id_get(trip_id)
```


# Authentication

This endpoint requires [furkot_auth_access_code](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md) **OR** [furkot_auth_implicit](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`Array[Step]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/models/structures/step.md).


# Example Usage

```ruby
trip_id = 'trip_id2'

result = client_api.trip_stop_by_trip_id_get(trip_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



