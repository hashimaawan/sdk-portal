# Update a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZVcGRhdGUlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Updates the description or labels of a Floating IP.
Also note that when updating labels, the Floating IP’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```python
def update_a_floating_ip(self,
                        id,
                        body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |
| `body` | [`UpdateFloatingIpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/update-floating-ip-request.md) | Body, Optional | - |


# Response Type

**200**: The `floating_ip` key in the reply contains the modified Floating IP object with the new description

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`FloatingIpsResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/floating-ips-response-2.md).


# Example Usage

```python
id = 112

body = UpdateFloatingIpRequest(
    description='Web Frontend',
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='Web Frontend'
)

result = floating_i_ps_api.update_a_floating_ip(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "floating_ip": {
    "blocked": false,
    "created": "2016-01-30T23:50:00+00:00",
    "description": "Web Frontend",
    "dns_ptr": [
      {
        "dns_ptr": "server.example.com",
        "ip": "2001:db8::1"
      }
    ],
    "home_location": {
      "city": "Falkenstein",
      "country": "DE",
      "description": "Falkenstein DC Park 1",
      "id": 1,
      "latitude": 50.47612,
      "longitude": 12.370071,
      "name": "fsn1",
      "network_zone": "eu-central"
    },
    "id": 4711,
    "ip": "131.232.99.1",
    "labels": {
      "labelkey": "value"
    },
    "name": "Web Frontend",
    "protection": {
      "delete": false
    },
    "server": 42,
    "type": "ipv4"
  }
}
```



