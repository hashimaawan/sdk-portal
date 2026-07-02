# Domain Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRvbWFpblJlY29yZA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`DomainRecord`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `String` | Optional | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. |
| `flags` | `Integer` | Optional | An unsigned integer between 0-255 used for CAA records. |
| `id` | `Integer` | Optional, Read-only | A unique identifier for each domain record. |
| `name` | `String` | Optional | The host name, alias, or service being defined by the record. |
| `port` | `Integer` | Optional | The port for SRV records. |
| `priority` | `Integer` | Optional | The priority for SRV and MX records. |
| `tag` | `String` | Optional | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" |
| `ttl` | `Integer` | Optional | This value is the time to live for the record, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. |
| `type` | `String` | Required | The type of the DNS record. For example: A, CNAME, TXT, ... |
| `weight` | `Integer` | Optional | The weight for SRV records. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
domain_record = DomainRecord.new(
  type: 'NS',
  data: 'ns1.digitalocean.com',
  flags: 132,
  id: 28448429,
  name: '@',
  port: 8,
  ttl: 1800,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



