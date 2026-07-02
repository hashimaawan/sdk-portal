# Domains Create Record Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRvbWFpbnNDcmVhdGVSZWNvcmRCb2R5


# Class Name

`DomainsCreateRecordBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2DomainsRecordsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-domains-records-request.md) | DomainsCreateRecordBody.FromV2DomainsRecordsRequest(V2DomainsRecordsRequest v2DomainsRecordsRequest) |
| [`V2DomainsRecordsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-domains-records-request-2.md) | DomainsCreateRecordBody.FromV2DomainsRecordsRequest2(V2DomainsRecordsRequest2 v2DomainsRecordsRequest2) |
| [`V2DomainsRecordsRequest4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-domains-records-request-4.md) | DomainsCreateRecordBody.FromV2DomainsRecordsRequest4(V2DomainsRecordsRequest4 v2DomainsRecordsRequest4) |
| [`V2DomainsRecordsRequest6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-domains-records-request-6.md) | DomainsCreateRecordBody.FromV2DomainsRecordsRequest6(V2DomainsRecordsRequest6 v2DomainsRecordsRequest6) |
| [`V2DomainsRecordsRequest7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-domains-records-request-7.md) | DomainsCreateRecordBody.FromV2DomainsRecordsRequest7(V2DomainsRecordsRequest7 v2DomainsRecordsRequest7) |


# V2DomainsRecordsRequest

## Initialization Code

### Example

```csharp
DomainsCreateRecordBody value = DomainsCreateRecordBody.FromV2DomainsRecordsRequest(
    new V2DomainsRecordsRequest
    {
        Data = "ns1.digitalocean.com",
        Name = "@",
        Type = "NS",
        Id = 28448429,
        Ttl = 1800,
    }
);
```


# V2DomainsRecordsRequest2

## Initialization Code

### Example

```csharp
DomainsCreateRecordBody value = DomainsCreateRecordBody.FromV2DomainsRecordsRequest2(
    new V2DomainsRecordsRequest2
    {
        Data = "ns1.digitalocean.com",
        Flags = null,
        Name = "@",
        Tag = null,
        Type = "NS",
        Id = 28448429,
        Ttl = 1800,
    }
);
```


# V2DomainsRecordsRequest4

## Initialization Code

### Example

```csharp
DomainsCreateRecordBody value = DomainsCreateRecordBody.FromV2DomainsRecordsRequest4(
    new V2DomainsRecordsRequest4
    {
        Data = "ns1.digitalocean.com",
        Priority = null,
        Type = "NS",
        Id = 28448429,
        Name = "@",
        Ttl = 1800,
    }
);
```


# V2DomainsRecordsRequest6

## Initialization Code

### Example

```csharp
DomainsCreateRecordBody value = DomainsCreateRecordBody.FromV2DomainsRecordsRequest6(
    new V2DomainsRecordsRequest6
    {
        Ttl = 1800,
        Type = "NS",
        Data = "ns1.digitalocean.com",
        Id = 28448429,
        Name = "@",
    }
);
```


# V2DomainsRecordsRequest7

## Initialization Code

### Example

```csharp
DomainsCreateRecordBody value = DomainsCreateRecordBody.FromV2DomainsRecordsRequest7(
    new V2DomainsRecordsRequest7
    {
        Data = "ns1.digitalocean.com",
        Flags = null,
        Name = "@",
        Port = null,
        Priority = null,
        Tag = null,
        Type = "NS",
        Id = 28448429,
        Ttl = 1800,
    }
);
```



