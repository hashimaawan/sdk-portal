# Droplet Actions Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRyb3BsZXRBY3Rpb25zUG9zdEJvZHk


# Class Name

`DropletActionsPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.V2DropletsActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-request.md) | models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest(models.V2DropletsActionsRequest v2DropletsActionsRequest) |
| [`models.V2DropletsActionsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-request-2.md) | models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest2(models.V2DropletsActionsRequest2 v2DropletsActionsRequest2) |
| [`models.V2DropletsActionsRequest21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-request-21.md) | models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest21(models.V2DropletsActionsRequest21 v2DropletsActionsRequest21) |
| [`models.V2DropletsActionsRequest22`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-request-22.md) | models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest22(models.V2DropletsActionsRequest22 v2DropletsActionsRequest22) |
| [`models.V2DropletsActionsRequest23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-request-23.md) | models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest23(models.V2DropletsActionsRequest23 v2DropletsActionsRequest23) |
| [`models.V2DropletsActionsRequest24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-request-24.md) | models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest24(models.V2DropletsActionsRequest24 v2DropletsActionsRequest24) |
| [`models.V2DropletsActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-request-1.md) | models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest1(models.V2DropletsActionsRequest1 v2DropletsActionsRequest1) |


# models.V2DropletsActionsRequest

## Initialization Code

### Example

```go
value := models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest(models.V2DropletsActionsRequest{
    Type:                  models.Type12_Reboot,
})
```


# models.V2DropletsActionsRequest2

## Initialization Code

### Example

```go
value := models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest2(models.V2DropletsActionsRequest2{
    Type:                  models.Type12_Reboot,
    Image:                 models.ToPointer(12389723),
})
```


# models.V2DropletsActionsRequest21

## Initialization Code

### Example

```go
value := models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest21(models.V2DropletsActionsRequest21{
    Type:                  models.Type12_Reboot,
    Disk:                  models.ToPointer(true),
    Size:                  models.ToPointer("s-2vcpu-2gb"),
})
```


# models.V2DropletsActionsRequest22

## Initialization Code

### Example

```go
value := models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest22(models.V2DropletsActionsRequest22{
    Type:                  models.Type12_Reboot,
    Image:                 models.ToPointer(models.V2DropletsActionsRequest22ImageContainer.FromString("ubuntu-20-04-x64")),
})
```


# models.V2DropletsActionsRequest23

## Initialization Code

### Example

```go
value := models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest23(models.V2DropletsActionsRequest23{
    Type:                  models.Type12_Reboot,
    Name:                  models.ToPointer("nifty-new-name"),
})
```


# models.V2DropletsActionsRequest24

## Initialization Code

### Example

```go
value := models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest24(models.V2DropletsActionsRequest24{
    Type:                  models.Type12_Reboot,
    Kernel:                models.ToPointer(12389723),
})
```


# models.V2DropletsActionsRequest1

## Initialization Code

### Example

```go
value := models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest1(models.V2DropletsActionsRequest1{
    Type:                  models.Type12_Reboot,
    Name:                  models.ToPointer("Nifty New Snapshot"),
})
```



