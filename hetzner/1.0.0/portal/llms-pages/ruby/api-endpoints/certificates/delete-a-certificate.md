# Delete a Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlcyUyRkRlbGV0ZSUyNTIwYSUyNTIwQ2VydGlmaWNhdGU

Deletes a Certificate.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def delete_a_certificate(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the resource |


# Response Type

**204**: Certificate deleted

`void`


# Example Usage

```ruby
id = 112

certificates_controller.delete_a_certificate(id)
```



