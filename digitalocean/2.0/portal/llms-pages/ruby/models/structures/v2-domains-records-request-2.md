# V2 Domains Records Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DomainsRecordsRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `String` | Required | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. |
| `flags` | `Integer` | Required | An unsigned integer between 0-255 used for CAA records. |
| `id` | `Integer` | Optional, Read-only | A unique identifier for each domain record. |
| `name` | `String` | Required | The host name, alias, or service being defined by the record. |
| `port` | `Integer` | Optional | The port for SRV records. |
| `priority` | `Integer` | Optional | The priority for SRV and MX records. |
| `tag` | `String` | Required | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" |
| `ttl` | `Integer` | Optional | This value is the time to live for the record, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. |
| `type` | `String` | Required | The type of the DNS record. For example: A, CNAME, TXT, ... |
| `weight` | `Integer` | Optional | The weight for SRV records. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_domains_records_request2 = V2DomainsRecordsRequest2.new(
  data: 'ns1.digitalocean.com',
  flags: nil,
  name: '@',
  tag: nil,
  type: 'NS',
  id: 28448429,
  port: 146,
  priority: 28,
  ttl: 1800,
  weight: 110,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



