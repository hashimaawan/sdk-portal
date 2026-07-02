# Domains Create Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkRvbWFpbiUyNTIwUmVjb3JkcyUyRmRvbWFpbnNfY3JlYXRlX3JlY29yZA

To create a new record to a domain, send a POST request to
`/v2/domains/$DOMAIN_NAME/records`.

The request must include all of the required fields for the domain record type
being added.

See the [attribute table](#tag/Domain-Records) for details regarding record
types and their respective required attributes.

```ruby
def domains_create_record(domain_name,
                          body: nil)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domain_name` | `String` | Template, Required | The name of the domain itself. |
| `body` | [V2 Domains Records Request](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-request.md) \| [V2 Domains Records Request2](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-request-2.md) \| [V2 Domains Records Request4](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-request-4.md) \| [V2 Domains Records Request6](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-request-6.md) \| [V2 Domains Records Request7](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-request-7.md) \| nil | Body, Optional | This is a container for any-of cases. |


# Response Type

**201**: The response body will be a JSON object with a key called `domain_record`. The value of this will be an object representing the new record. Attributes that are not applicable for the record type will be set to `null`. An `id` attribute is generated for each record as part of the object.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2DomainsRecordsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-response-1.md).


# Example Usage

```ruby
domain_name = 'example.com'

body = V2DomainsRecordsRequest.new(
  data: '162.10.66.0',
  name: 'www',
  type: 'A',
  flags: nil,
  port: nil,
  priority: nil,
  tag: nil,
  ttl: 1800,
  weight: nil
)

result = domain_records_api.domains_create_record(
  domain_name,
  body: body
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



