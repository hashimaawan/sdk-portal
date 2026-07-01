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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
id = 112

result = certificates_api.delete_a_certificate(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



