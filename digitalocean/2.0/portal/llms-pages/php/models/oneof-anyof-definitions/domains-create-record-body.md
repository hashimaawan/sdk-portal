# Domains Create Record Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRvbWFpbnNDcmVhdGVSZWNvcmRCb2R5


# Data Type

`V2DomainsRecordsRequest|V2DomainsRecordsRequest2|V2DomainsRecordsRequest4|V2DomainsRecordsRequest6|V2DomainsRecordsRequest7`


# Cases

| Type |
|  --- |
| [`V2DomainsRecordsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-domains-records-request.md) |
| [`V2DomainsRecordsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-domains-records-request-2.md) |
| [`V2DomainsRecordsRequest4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-domains-records-request-4.md) |
| [`V2DomainsRecordsRequest6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-domains-records-request-6.md) |
| [`V2DomainsRecordsRequest7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-domains-records-request-7.md) |


# V2DomainsRecordsRequest

## Initialization Code

### Example

```php
$value = V2DomainsRecordsRequestBuilder::init(
    'ns1.digitalocean.com',
    '@',
    'NS'
)
    ->id(28448429)
    ->ttl(1800)
    ->build();
```


# V2DomainsRecordsRequest2

## Initialization Code

### Example

```php
$value = V2DomainsRecordsRequest2Builder::init(
    'ns1.digitalocean.com',
    '@',
    'NS'
)
    ->flags(null)
    ->id(28448429)
    ->tag(null)
    ->ttl(1800)
    ->build();
```


# V2DomainsRecordsRequest4

## Initialization Code

### Example

```php
$value = V2DomainsRecordsRequest4Builder::init(
    'ns1.digitalocean.com',
    'NS'
)
    ->id(28448429)
    ->name('@')
    ->priority(null)
    ->ttl(1800)
    ->build();
```


# V2DomainsRecordsRequest6

## Initialization Code

### Example

```php
$value = V2DomainsRecordsRequest6Builder::init(
    1800,
    'NS'
)
    ->data('ns1.digitalocean.com')
    ->id(28448429)
    ->name('@')
    ->build();
```


# V2DomainsRecordsRequest7

## Initialization Code

### Example

```php
$value = V2DomainsRecordsRequest7Builder::init(
    'ns1.digitalocean.com',
    '@',
    'NS'
)
    ->flags(null)
    ->id(28448429)
    ->port(null)
    ->priority(null)
    ->tag(null)
    ->ttl(1800)
    ->build();
```



