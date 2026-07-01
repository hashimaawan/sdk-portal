# Trip Stop by Trip Id GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRlRyaXBTdG9wQnlUcmlwSWRfR0VU

list stops for a trip identified by {trip_id}

```python
def trip_stop_by_trip_id_get(self,
                            trip_id)
```


# Authentication

This endpoint requires [furkot_auth_access_code](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/getting-started/quickstart/authorization.md) **OR** [furkot_auth_implicit](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `trip_id` | `str` | Template, Required | id of the trip |


# Requires scope

## furkot_auth_access_code

`read:trips`

## furkot_auth_implicit

`read:trips`


# Response Type

**200**: Successful response

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`List[Step]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/models/structures/step.md).


# Example Usage

```python
trip_id = 'trip_id2'

result = client_api.trip_stop_by_trip_id_get(trip_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



