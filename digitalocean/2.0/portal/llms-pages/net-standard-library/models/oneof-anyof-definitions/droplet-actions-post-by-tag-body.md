# Droplet Actions Post by Tag Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRyb3BsZXRBY3Rpb25zUG9zdEJ5VGFnQm9keQ


# Class Name

`DropletActionsPostByTagBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2DropletsActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-droplets-actions-request.md) | DropletActionsPostByTagBody.FromV2DropletsActionsRequest(V2DropletsActionsRequest v2DropletsActionsRequest) |
| [`V2DropletsActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-droplets-actions-request-1.md) | DropletActionsPostByTagBody.FromV2DropletsActionsRequest1(V2DropletsActionsRequest1 v2DropletsActionsRequest1) |


# V2DropletsActionsRequest

## Initialization Code

### Example

```csharp
DropletActionsPostByTagBody value = DropletActionsPostByTagBody.FromV2DropletsActionsRequest(
    new V2DropletsActionsRequest
    {
        Type = Type12.Reboot,
    }
);
```


# V2DropletsActionsRequest1

## Initialization Code

### Example

```csharp
DropletActionsPostByTagBody value = DropletActionsPostByTagBody.FromV2DropletsActionsRequest1(
    new V2DropletsActionsRequest1
    {
        Type = Type12.Reboot,
        Name = "Nifty New Snapshot",
    }
);
```



