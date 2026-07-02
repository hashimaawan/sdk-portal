# Domains Create Record Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRvbWFpbnNDcmVhdGVSZWNvcmRCb2R5


# Class Name

`DomainsCreateRecordBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2DomainsRecordsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-domains-records-request.md) | DomainsCreateRecordBody.fromV2DomainsRecordsRequest(V2DomainsRecordsRequest v2DomainsRecordsRequest) |
| [`V2DomainsRecordsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-domains-records-request-2.md) | DomainsCreateRecordBody.fromV2DomainsRecordsRequest2(V2DomainsRecordsRequest2 v2DomainsRecordsRequest2) |
| [`V2DomainsRecordsRequest4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-domains-records-request-4.md) | DomainsCreateRecordBody.fromV2DomainsRecordsRequest4(V2DomainsRecordsRequest4 v2DomainsRecordsRequest4) |
| [`V2DomainsRecordsRequest6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-domains-records-request-6.md) | DomainsCreateRecordBody.fromV2DomainsRecordsRequest6(V2DomainsRecordsRequest6 v2DomainsRecordsRequest6) |
| [`V2DomainsRecordsRequest7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-domains-records-request-7.md) | DomainsCreateRecordBody.fromV2DomainsRecordsRequest7(V2DomainsRecordsRequest7 v2DomainsRecordsRequest7) |


# V2DomainsRecordsRequest

## Initialization Code

### Example

```java
DomainsCreateRecordBody.fromV2DomainsRecordsRequest(
        new V2DomainsRecordsRequest.Builder(
            "ns1.digitalocean.com",
            "@",
            "NS"
        )
        .id(28448429)
        .ttl(1800)
        .build()
    )
```


# V2DomainsRecordsRequest2

## Initialization Code

### Example

```java
DomainsCreateRecordBody.fromV2DomainsRecordsRequest2(
        new V2DomainsRecordsRequest2.Builder(
            "ns1.digitalocean.com",
            null,
            "@",
            null,
            "NS"
        )
        .id(28448429)
        .ttl(1800)
        .build()
    )
```


# V2DomainsRecordsRequest4

## Initialization Code

### Example

```java
DomainsCreateRecordBody.fromV2DomainsRecordsRequest4(
        new V2DomainsRecordsRequest4.Builder(
            "ns1.digitalocean.com",
            null,
            "NS"
        )
        .id(28448429)
        .name("@")
        .ttl(1800)
        .build()
    )
```


# V2DomainsRecordsRequest6

## Initialization Code

### Example

```java
DomainsCreateRecordBody.fromV2DomainsRecordsRequest6(
        new V2DomainsRecordsRequest6.Builder(
            1800,
            "NS"
        )
        .data("ns1.digitalocean.com")
        .id(28448429)
        .name("@")
        .build()
    )
```


# V2DomainsRecordsRequest7

## Initialization Code

### Example

```java
DomainsCreateRecordBody.fromV2DomainsRecordsRequest7(
        new V2DomainsRecordsRequest7.Builder(
            "ns1.digitalocean.com",
            null,
            "@",
            null,
            null,
            null,
            "NS"
        )
        .id(28448429)
        .ttl(1800)
        .build()
    )
```



