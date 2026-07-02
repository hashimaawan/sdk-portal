# Droplets Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRyb3BsZXRzQ3JlYXRlQm9keQ


# Class Name

`DropletsCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.SingleDropletRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/single-droplet-request.md) | models.DropletsCreateBodyContainer.FromSingleDropletRequest(models.SingleDropletRequest singleDropletRequest) |
| [`models.MultipleDropletRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/multiple-droplet-request.md) | models.DropletsCreateBodyContainer.FromMultipleDropletRequest(models.MultipleDropletRequest multipleDropletRequest) |


# models.SingleDropletRequest

## Initialization Code

### Example

```go
value := models.DropletsCreateBodyContainer.FromSingleDropletRequest(models.SingleDropletRequest{
    Name:                  "example.com",
    Backups:               models.ToPointer(true),
    Image:                 models.SingleDropletRequestImageContainer.FromString("ubuntu-20-04-x64"),
    Ipv6:                  models.ToPointer(true),
    Monitoring:            models.ToPointer(true),
    PrivateNetworking:     models.ToPointer(true),
    Region:                models.ToPointer("nyc3"),
    Size:                  "s-1vcpu-1gb",
    SshKeys:               []models.SingleDropletRequestSshKeys{
        models.SingleDropletRequestSshKeysContainer.FromNumber(289794),
        models.SingleDropletRequestSshKeysContainer.FromString("3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45"),
    },
    Tags:                  models.NewOptional(models.ToPointer([]string{
        "env:prod",
        "web",
    })),
    UserData:              models.ToPointer("#cloud-config\nruncmd:\n  - touch /test.txt\n"),
    Volumes:               []string{
        "12e97116-7280-11ed-b3d0-0a58ac146812",
    },
    VpcUuid:               models.ToPointer("760e09ef-dc84-11e8-981e-3cfdfeaae000"),
    WithDropletAgent:      models.ToPointer(true),
})
```


# models.MultipleDropletRequest

## Initialization Code

### Example

```go
value := models.DropletsCreateBodyContainer.FromMultipleDropletRequest(models.MultipleDropletRequest{
    Names:                 []string{
        "sub-01.example.com",
        "sub-02.example.com",
    },
    Backups:               models.ToPointer(true),
    Image:                 models.MultipleDropletRequestImageContainer.FromString("ubuntu-20-04-x64"),
    Ipv6:                  models.ToPointer(true),
    Monitoring:            models.ToPointer(true),
    PrivateNetworking:     models.ToPointer(true),
    Region:                models.ToPointer("nyc3"),
    Size:                  "s-1vcpu-1gb",
    SshKeys:               []models.MultipleDropletRequestSshKeys{
        models.MultipleDropletRequestSshKeysContainer.FromNumber(289794),
        models.MultipleDropletRequestSshKeysContainer.FromString("3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45"),
    },
    Tags:                  models.NewOptional(models.ToPointer([]string{
        "env:prod",
        "web",
    })),
    UserData:              models.ToPointer("#cloud-config\nruncmd:\n  - touch /test.txt\n"),
    Volumes:               []string{
        "12e97116-7280-11ed-b3d0-0a58ac146812",
    },
    VpcUuid:               models.ToPointer("760e09ef-dc84-11e8-981e-3cfdfeaae000"),
    WithDropletAgent:      models.ToPointer(true),
})
```



