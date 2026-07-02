# Droplet Actions Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRyb3BsZXRBY3Rpb25zUG9zdEJvZHk


# Class Name

`DropletActionsPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2DropletsActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-droplets-actions-request.md) | DropletActionsPostBody.FromV2DropletsActionsRequest(V2DropletsActionsRequest v2DropletsActionsRequest) |
| [`V2DropletsActionsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-droplets-actions-request-2.md) | DropletActionsPostBody.FromV2DropletsActionsRequest2(V2DropletsActionsRequest2 v2DropletsActionsRequest2) |
| [`V2DropletsActionsRequest21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-droplets-actions-request-21.md) | DropletActionsPostBody.FromV2DropletsActionsRequest21(V2DropletsActionsRequest21 v2DropletsActionsRequest21) |
| [`V2DropletsActionsRequest22`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-droplets-actions-request-22.md) | DropletActionsPostBody.FromV2DropletsActionsRequest22(V2DropletsActionsRequest22 v2DropletsActionsRequest22) |
| [`V2DropletsActionsRequest23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-droplets-actions-request-23.md) | DropletActionsPostBody.FromV2DropletsActionsRequest23(V2DropletsActionsRequest23 v2DropletsActionsRequest23) |
| [`V2DropletsActionsRequest24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-droplets-actions-request-24.md) | DropletActionsPostBody.FromV2DropletsActionsRequest24(V2DropletsActionsRequest24 v2DropletsActionsRequest24) |
| [`V2DropletsActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-droplets-actions-request-1.md) | DropletActionsPostBody.FromV2DropletsActionsRequest1(V2DropletsActionsRequest1 v2DropletsActionsRequest1) |


# V2DropletsActionsRequest

## Initialization Code

### Example

```csharp
DropletActionsPostBody value = DropletActionsPostBody.FromV2DropletsActionsRequest(
    new V2DropletsActionsRequest
    {
        Type = Type12.Reboot,
    }
);
```


# V2DropletsActionsRequest2

## Initialization Code

### Example

```csharp
DropletActionsPostBody value = DropletActionsPostBody.FromV2DropletsActionsRequest2(
    new V2DropletsActionsRequest2
    {
        Type = Type12.Reboot,
        Image = 12389723,
    }
);
```


# V2DropletsActionsRequest21

## Initialization Code

### Example

```csharp
DropletActionsPostBody value = DropletActionsPostBody.FromV2DropletsActionsRequest21(
    new V2DropletsActionsRequest21
    {
        Type = Type12.Reboot,
        Disk = true,
        Size = "s-2vcpu-2gb",
    }
);
```


# V2DropletsActionsRequest22

## Initialization Code

### Example

```csharp
DropletActionsPostBody value = DropletActionsPostBody.FromV2DropletsActionsRequest22(
    new V2DropletsActionsRequest22
    {
        Type = Type12.Reboot,
        Image = V2DropletsActionsRequest22Image.FromString("ubuntu-20-04-x64"),
    }
);
```


# V2DropletsActionsRequest23

## Initialization Code

### Example

```csharp
DropletActionsPostBody value = DropletActionsPostBody.FromV2DropletsActionsRequest23(
    new V2DropletsActionsRequest23
    {
        Type = Type12.Reboot,
        Name = "nifty-new-name",
    }
);
```


# V2DropletsActionsRequest24

## Initialization Code

### Example

```csharp
DropletActionsPostBody value = DropletActionsPostBody.FromV2DropletsActionsRequest24(
    new V2DropletsActionsRequest24
    {
        Type = Type12.Reboot,
        Kernel = 12389723,
    }
);
```


# V2DropletsActionsRequest1

## Initialization Code

### Example

```csharp
DropletActionsPostBody value = DropletActionsPostBody.FromV2DropletsActionsRequest1(
    new V2DropletsActionsRequest1
    {
        Type = Type12.Reboot,
        Name = "Nifty New Snapshot",
    }
);
```



