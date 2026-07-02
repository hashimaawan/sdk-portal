# Droplet Actions Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRyb3BsZXRBY3Rpb25zUG9zdEJvZHk


# Class Name

`DropletActionsPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2DropletsActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-actions-request.md) | DropletActionsPostBody.fromV2DropletsActionsRequest(V2DropletsActionsRequest v2DropletsActionsRequest) |
| [`V2DropletsActionsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-actions-request-2.md) | DropletActionsPostBody.fromV2DropletsActionsRequest2(V2DropletsActionsRequest2 v2DropletsActionsRequest2) |
| [`V2DropletsActionsRequest21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-actions-request-21.md) | DropletActionsPostBody.fromV2DropletsActionsRequest21(V2DropletsActionsRequest21 v2DropletsActionsRequest21) |
| [`V2DropletsActionsRequest22`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-actions-request-22.md) | DropletActionsPostBody.fromV2DropletsActionsRequest22(V2DropletsActionsRequest22 v2DropletsActionsRequest22) |
| [`V2DropletsActionsRequest23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-actions-request-23.md) | DropletActionsPostBody.fromV2DropletsActionsRequest23(V2DropletsActionsRequest23 v2DropletsActionsRequest23) |
| [`V2DropletsActionsRequest24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-actions-request-24.md) | DropletActionsPostBody.fromV2DropletsActionsRequest24(V2DropletsActionsRequest24 v2DropletsActionsRequest24) |
| [`V2DropletsActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-actions-request-1.md) | DropletActionsPostBody.fromV2DropletsActionsRequest1(V2DropletsActionsRequest1 v2DropletsActionsRequest1) |


# V2DropletsActionsRequest

## Initialization Code

### Example

```java
DropletActionsPostBody.fromV2DropletsActionsRequest(
        new V2DropletsActionsRequest.Builder(
            Type12.REBOOT
        )
        .build()
    )
```


# V2DropletsActionsRequest2

## Initialization Code

### Example

```java
DropletActionsPostBody.fromV2DropletsActionsRequest2(
        new V2DropletsActionsRequest2.Builder(
            Type12.REBOOT
        )
        .image(12389723)
        .build()
    )
```


# V2DropletsActionsRequest21

## Initialization Code

### Example

```java
DropletActionsPostBody.fromV2DropletsActionsRequest21(
        new V2DropletsActionsRequest21.Builder(
            Type12.REBOOT
        )
        .disk(true)
        .size("s-2vcpu-2gb")
        .build()
    )
```


# V2DropletsActionsRequest22

## Initialization Code

### Example

```java
DropletActionsPostBody.fromV2DropletsActionsRequest22(
        new V2DropletsActionsRequest22.Builder(
            Type12.REBOOT
        )
        .image(V2DropletsActionsRequest22Image.fromString(
                "ubuntu-20-04-x64"
            ))
        .build()
    )
```


# V2DropletsActionsRequest23

## Initialization Code

### Example

```java
DropletActionsPostBody.fromV2DropletsActionsRequest23(
        new V2DropletsActionsRequest23.Builder(
            Type12.REBOOT
        )
        .name("nifty-new-name")
        .build()
    )
```


# V2DropletsActionsRequest24

## Initialization Code

### Example

```java
DropletActionsPostBody.fromV2DropletsActionsRequest24(
        new V2DropletsActionsRequest24.Builder(
            Type12.REBOOT
        )
        .kernel(12389723)
        .build()
    )
```


# V2DropletsActionsRequest1

## Initialization Code

### Example

```java
DropletActionsPostBody.fromV2DropletsActionsRequest1(
        new V2DropletsActionsRequest1.Builder(
            Type12.REBOOT
        )
        .name("Nifty New Snapshot")
        .build()
    )
```



