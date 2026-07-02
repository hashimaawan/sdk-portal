# Domains Create Record Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRvbWFpbnNDcmVhdGVSZWNvcmRCb2R5


# Data Type

`V2DomainsRecordsRequest | V2DomainsRecordsRequest2 | V2DomainsRecordsRequest4 | V2DomainsRecordsRequest6 | V2DomainsRecordsRequest7`


# Cases

| Type |
|  --- |
| [`V2DomainsRecordsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-request.md) |
| [`V2DomainsRecordsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-request-2.md) |
| [`V2DomainsRecordsRequest4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-request-4.md) |
| [`V2DomainsRecordsRequest6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-request-6.md) |
| [`V2DomainsRecordsRequest7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-domains-records-request-7.md) |


# V2DomainsRecordsRequest

## Initialization Code

### Example

```ruby
value = V2DomainsRecordsRequest.new(
  data: 'ns1.digitalocean.com',
  name: '@',
  type: 'NS',
  id: 28448429,
  ttl: 1800
)
```


# V2DomainsRecordsRequest2

## Initialization Code

### Example

```ruby
value = V2DomainsRecordsRequest2.new(
  data: 'ns1.digitalocean.com',
  flags: nil,
  name: '@',
  tag: nil,
  type: 'NS',
  id: 28448429,
  ttl: 1800
)
```


# V2DomainsRecordsRequest4

## Initialization Code

### Example

```ruby
value = V2DomainsRecordsRequest4.new(
  data: 'ns1.digitalocean.com',
  priority: nil,
  type: 'NS',
  id: 28448429,
  name: '@',
  ttl: 1800
)
```


# V2DomainsRecordsRequest6

## Initialization Code

### Example

```ruby
value = V2DomainsRecordsRequest6.new(
  ttl: 1800,
  type: 'NS',
  data: 'ns1.digitalocean.com',
  id: 28448429,
  name: '@'
)
```


# V2DomainsRecordsRequest7

## Initialization Code

### Example

```ruby
value = V2DomainsRecordsRequest7.new(
  data: 'ns1.digitalocean.com',
  flags: nil,
  name: '@',
  port: nil,
  priority: nil,
  tag: nil,
  type: 'NS',
  id: 28448429,
  ttl: 1800
)
```



