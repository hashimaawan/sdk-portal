# Domains Create Record Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkRvbWFpbnNDcmVhdGVSZWNvcmRCb2R5


# Class Name

`DomainsCreateRecordBody`


# Cases

| Type |
|  --- |
| [`V2DomainsRecordsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-domains-records-request.md) |
| [`V2DomainsRecordsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-domains-records-request-2.md) |
| [`V2DomainsRecordsRequest4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-domains-records-request-4.md) |
| [`V2DomainsRecordsRequest6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-domains-records-request-6.md) |
| [`V2DomainsRecordsRequest7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-domains-records-request-7.md) |


# V2DomainsRecordsRequest

## Initialization Code

### Example

```ts
const value: DomainsCreateRecordBody = {
  data: 'ns1.digitalocean.com',
  name: '@',
  type: 'NS',
  id: 28448429,
  ttl: 1800,
};
```


# V2DomainsRecordsRequest2

## Initialization Code

### Example

```ts
const value: DomainsCreateRecordBody = {
  data: 'ns1.digitalocean.com',
  flags: null,
  name: '@',
  tag: null,
  type: 'NS',
  id: 28448429,
  ttl: 1800,
};
```


# V2DomainsRecordsRequest4

## Initialization Code

### Example

```ts
const value: DomainsCreateRecordBody = {
  data: 'ns1.digitalocean.com',
  priority: null,
  type: 'NS',
  id: 28448429,
  name: '@',
  ttl: 1800,
};
```


# V2DomainsRecordsRequest6

## Initialization Code

### Example

```ts
const value: DomainsCreateRecordBody = {
  ttl: 1800,
  type: 'NS',
  data: 'ns1.digitalocean.com',
  id: 28448429,
  name: '@',
};
```


# V2DomainsRecordsRequest7

## Initialization Code

### Example

```ts
const value: DomainsCreateRecordBody = {
  data: 'ns1.digitalocean.com',
  flags: null,
  name: '@',
  port: null,
  priority: null,
  tag: null,
  type: 'NS',
  id: 28448429,
  ttl: 1800,
};
```



