# Droplet Actions Post by Tag Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRyb3BsZXRBY3Rpb25zUG9zdEJ5VGFnQm9keQ


# Class Name

`DropletActionsPostByTagBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.V2DropletsActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-request.md) | models.DropletActionsPostByTagBodyContainer.FromV2DropletsActionsRequest(models.V2DropletsActionsRequest v2DropletsActionsRequest) |
| [`models.V2DropletsActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-request-1.md) | models.DropletActionsPostByTagBodyContainer.FromV2DropletsActionsRequest1(models.V2DropletsActionsRequest1 v2DropletsActionsRequest1) |


# models.V2DropletsActionsRequest

## Initialization Code

### Example

```go
value := models.DropletActionsPostByTagBodyContainer.FromV2DropletsActionsRequest(models.V2DropletsActionsRequest{
    Type:                  models.Type12_Reboot,
})
```


# models.V2DropletsActionsRequest1

## Initialization Code

### Example

```go
value := models.DropletActionsPostByTagBodyContainer.FromV2DropletsActionsRequest1(models.V2DropletsActionsRequest1{
    Type:                  models.Type12_Reboot,
    Name:                  models.ToPointer("Nifty New Snapshot"),
})
```



