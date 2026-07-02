# Firewalls List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRmZpcmV3YWxsc19saXN0

To list all of the firewalls available on your account, send a GET request to `/v2/firewalls`.

```python
def firewalls_list(self,
                  per_page=20,
                  page=1)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `per_page` | `int` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `int` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: To list all of the firewalls available on your account, send a GET request to `/v2/firewalls`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2FirewallsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-firewalls-response.md).


# Example Usage

```python
per_page = 2

page = 1

result = firewalls_api.firewalls_list(
    per_page=per_page,
    page=page
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "firewalls": [
    {
      "created_at": "2017-05-23T21:23:59Z",
      "droplet_ids": [
        8043964
      ],
      "id": "fb6045f1-cf1d-4ca3-bfac-18832663025b",
      "inbound_rules": [
        {
          "ports": "80",
          "protocol": "tcp",
          "sources": {
            "load_balancer_uids": [
              "4de7ac8b-495b-4884-9a69-1050c6793cd6"
            ]
          }
        },
        {
          "ports": "22",
          "protocol": "tcp",
          "sources": {
            "addresses": [
              "18.0.0.0/8"
            ],
            "tags": [
              "gateway"
            ]
          }
        }
      ],
      "name": "firewall",
      "outbound_rules": [
        {
          "destinations": {
            "addresses": [
              "0.0.0.0/0",
              "::/0"
            ]
          },
          "ports": "80",
          "protocol": "tcp"
        }
      ],
      "pending_changes": [],
      "status": "succeeded",
      "tags": []
    }
  ],
  "links": {},
  "meta": {
    "total": 1
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



