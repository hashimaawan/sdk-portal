# Droplets Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRyb3BsZXRzQ3JlYXRlQm9keQ


# Class Name

`DropletsCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`SingleDropletRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/single-droplet-request.md) | DropletsCreateBody.FromSingleDropletRequest(SingleDropletRequest singleDropletRequest) |
| [`MultipleDropletRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/multiple-droplet-request.md) | DropletsCreateBody.FromMultipleDropletRequest(MultipleDropletRequest multipleDropletRequest) |


# SingleDropletRequest

## Initialization Code

### Example

```csharp
DropletsCreateBody value = DropletsCreateBody.FromSingleDropletRequest(
    new SingleDropletRequest
    {
        Name = "example.com",
        Image = SingleDropletRequestImage.FromString("ubuntu-20-04-x64"),
        Size = "s-1vcpu-1gb",
        Backups = true,
        Ipv6 = true,
        Monitoring = true,
        PrivateNetworking = true,
        Region = "nyc3",
        SshKeys = new List<SingleDropletRequestSshKeys>
        {
            SingleDropletRequestSshKeys.FromNumber(289794),
            SingleDropletRequestSshKeys.FromString("3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45"),
        },
        Tags = new List<string>
        {
            "env:prod",
            "web",
        },
        UserData = "#cloud-config\nruncmd:\n  - touch /test.txt\n",
        Volumes = new List<string>
        {
            "12e97116-7280-11ed-b3d0-0a58ac146812",
        },
        VpcUuid = "760e09ef-dc84-11e8-981e-3cfdfeaae000",
        WithDropletAgent = true,
    }
);
```


# MultipleDropletRequest

## Initialization Code

### Example

```csharp
DropletsCreateBody value = DropletsCreateBody.FromMultipleDropletRequest(
    new MultipleDropletRequest
    {
        Names = new List<string>
        {
            "sub-01.example.com",
            "sub-02.example.com",
        },
        Image = MultipleDropletRequestImage.FromString("ubuntu-20-04-x64"),
        Size = "s-1vcpu-1gb",
        Backups = true,
        Ipv6 = true,
        Monitoring = true,
        PrivateNetworking = true,
        Region = "nyc3",
        SshKeys = new List<MultipleDropletRequestSshKeys>
        {
            MultipleDropletRequestSshKeys.FromNumber(289794),
            MultipleDropletRequestSshKeys.FromString("3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45"),
        },
        Tags = new List<string>
        {
            "env:prod",
            "web",
        },
        UserData = "#cloud-config\nruncmd:\n  - touch /test.txt\n",
        Volumes = new List<string>
        {
            "12e97116-7280-11ed-b3d0-0a58ac146812",
        },
        VpcUuid = "760e09ef-dc84-11e8-981e-3cfdfeaae000",
        WithDropletAgent = true,
    }
);
```



