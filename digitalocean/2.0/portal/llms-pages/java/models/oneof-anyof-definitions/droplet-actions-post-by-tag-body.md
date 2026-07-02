# Droplet Actions Post by Tag Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRyb3BsZXRBY3Rpb25zUG9zdEJ5VGFnQm9keQ


# Class Name

`DropletActionsPostByTagBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2DropletsActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-actions-request.md) | DropletActionsPostByTagBody.fromV2DropletsActionsRequest(V2DropletsActionsRequest v2DropletsActionsRequest) |
| [`V2DropletsActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-actions-request-1.md) | DropletActionsPostByTagBody.fromV2DropletsActionsRequest1(V2DropletsActionsRequest1 v2DropletsActionsRequest1) |


# V2DropletsActionsRequest

## Initialization Code

### Example

```java
DropletActionsPostByTagBody.fromV2DropletsActionsRequest(
        new V2DropletsActionsRequest.Builder(
            Type12.REBOOT
        )
        .build()
    )
```


# V2DropletsActionsRequest1

## Initialization Code

### Example

```java
DropletActionsPostByTagBody.fromV2DropletsActionsRequest1(
        new V2DropletsActionsRequest1.Builder(
            Type12.REBOOT
        )
        .name("Nifty New Snapshot")
        .build()
    )
```



