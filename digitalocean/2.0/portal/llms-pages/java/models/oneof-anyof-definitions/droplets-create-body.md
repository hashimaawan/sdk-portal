# Droplets Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRyb3BsZXRzQ3JlYXRlQm9keQ


# Class Name

`DropletsCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`SingleDropletRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/single-droplet-request.md) | DropletsCreateBody.fromSingleDropletRequest(SingleDropletRequest singleDropletRequest) |
| [`MultipleDropletRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/multiple-droplet-request.md) | DropletsCreateBody.fromMultipleDropletRequest(MultipleDropletRequest multipleDropletRequest) |


# SingleDropletRequest

## Initialization Code

### Example

```java
DropletsCreateBody.fromSingleDropletRequest(
        new SingleDropletRequest.Builder(
            "example.com",
            SingleDropletRequestImage.fromString(
                "ubuntu-20-04-x64"
            ),
            "s-1vcpu-1gb"
        )
        .backups(true)
        .ipv6(true)
        .monitoring(true)
        .privateNetworking(true)
        .region("nyc3")
        .sshKeys(Arrays.asList(
                SingleDropletRequestSshKeys.fromNumber(
                    289794
                ),
                SingleDropletRequestSshKeys.fromString(
                    "3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45"
                )
            ))
        .tags(Arrays.asList(
                "env:prod",
                "web"
            ))
        .userData("#cloud-config\nruncmd:\n  - touch /test.txt\n")
        .volumes(Arrays.asList(
                "12e97116-7280-11ed-b3d0-0a58ac146812"
            ))
        .vpcUuid("760e09ef-dc84-11e8-981e-3cfdfeaae000")
        .withDropletAgent(true)
        .build()
    )
```


# MultipleDropletRequest

## Initialization Code

### Example

```java
DropletsCreateBody.fromMultipleDropletRequest(
        new MultipleDropletRequest.Builder(
            Arrays.asList(
                "sub-01.example.com",
                "sub-02.example.com"
            ),
            MultipleDropletRequestImage.fromString(
                "ubuntu-20-04-x64"
            ),
            "s-1vcpu-1gb"
        )
        .backups(true)
        .ipv6(true)
        .monitoring(true)
        .privateNetworking(true)
        .region("nyc3")
        .sshKeys(Arrays.asList(
                MultipleDropletRequestSshKeys.fromNumber(
                    289794
                ),
                MultipleDropletRequestSshKeys.fromString(
                    "3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45"
                )
            ))
        .tags(Arrays.asList(
                "env:prod",
                "web"
            ))
        .userData("#cloud-config\nruncmd:\n  - touch /test.txt\n")
        .volumes(Arrays.asList(
                "12e97116-7280-11ed-b3d0-0a58ac146812"
            ))
        .vpcUuid("760e09ef-dc84-11e8-981e-3cfdfeaae000")
        .withDropletAgent(true)
        .build()
    )
```



