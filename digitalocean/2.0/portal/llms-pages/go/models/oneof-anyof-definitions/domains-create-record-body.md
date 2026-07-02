# Domains Create Record Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRvbWFpbnNDcmVhdGVSZWNvcmRCb2R5


# Class Name

`DomainsCreateRecordBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.V2DomainsRecordsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-domains-records-request.md) | models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest(models.V2DomainsRecordsRequest v2DomainsRecordsRequest) |
| [`models.V2DomainsRecordsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-domains-records-request-2.md) | models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest2(models.V2DomainsRecordsRequest2 v2DomainsRecordsRequest2) |
| [`models.V2DomainsRecordsRequest4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-domains-records-request-4.md) | models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest4(models.V2DomainsRecordsRequest4 v2DomainsRecordsRequest4) |
| [`models.V2DomainsRecordsRequest6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-domains-records-request-6.md) | models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest6(models.V2DomainsRecordsRequest6 v2DomainsRecordsRequest6) |
| [`models.V2DomainsRecordsRequest7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-domains-records-request-7.md) | models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest7(models.V2DomainsRecordsRequest7 v2DomainsRecordsRequest7) |


# models.V2DomainsRecordsRequest

## Initialization Code

### Example

```go
value := models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest(models.V2DomainsRecordsRequest{
    Data:                  "ns1.digitalocean.com",
    Id:                    models.ToPointer(28448429),
    Name:                  "@",
    Ttl:                   models.ToPointer(1800),
    Type:                  "NS",
})
```


# models.V2DomainsRecordsRequest2

## Initialization Code

### Example

```go
value := models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest2(models.V2DomainsRecordsRequest2{
    Data:                  "ns1.digitalocean.com",
    Flags:                 nil,
    Id:                    models.ToPointer(28448429),
    Name:                  "@",
    Tag:                   nil,
    Ttl:                   models.ToPointer(1800),
    Type:                  "NS",
})
```


# models.V2DomainsRecordsRequest4

## Initialization Code

### Example

```go
value := models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest4(models.V2DomainsRecordsRequest4{
    Data:                  "ns1.digitalocean.com",
    Id:                    models.ToPointer(28448429),
    Name:                  models.ToPointer("@"),
    Priority:              nil,
    Ttl:                   models.ToPointer(1800),
    Type:                  "NS",
})
```


# models.V2DomainsRecordsRequest6

## Initialization Code

### Example

```go
value := models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest6(models.V2DomainsRecordsRequest6{
    Data:                  models.ToPointer("ns1.digitalocean.com"),
    Id:                    models.ToPointer(28448429),
    Name:                  models.ToPointer("@"),
    Ttl:                   1800,
    Type:                  "NS",
})
```


# models.V2DomainsRecordsRequest7

## Initialization Code

### Example

```go
value := models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest7(models.V2DomainsRecordsRequest7{
    Data:                  "ns1.digitalocean.com",
    Flags:                 nil,
    Id:                    models.ToPointer(28448429),
    Name:                  "@",
    Port:                  nil,
    Priority:              nil,
    Tag:                   nil,
    Ttl:                   models.ToPointer(1800),
    Type:                  "NS",
})
```



