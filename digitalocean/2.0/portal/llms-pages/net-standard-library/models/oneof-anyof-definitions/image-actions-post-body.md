# Image Actions Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdlQWN0aW9uc1Bvc3RCb2R5


# Class Name

`ImageActionsPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2ImagesActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-images-actions-request.md) | ImageActionsPostBody.FromV2ImagesActionsRequest(V2ImagesActionsRequest v2ImagesActionsRequest) |
| [`V2ImagesActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-images-actions-request-1.md) | ImageActionsPostBody.FromV2ImagesActionsRequest1(V2ImagesActionsRequest1 v2ImagesActionsRequest1) |


# V2ImagesActionsRequest

## Initialization Code

### Example

```csharp
ImageActionsPostBody value = ImageActionsPostBody.FromV2ImagesActionsRequest(
    new V2ImagesActionsRequest
    {
        Type = Type15.Convert,
    }
);
```


# V2ImagesActionsRequest1

## Initialization Code

### Example

```csharp
ImageActionsPostBody value = ImageActionsPostBody.FromV2ImagesActionsRequest1(
    new V2ImagesActionsRequest1
    {
        Type = Type15.Convert,
        Region = Region2.Nyc3,
    }
);
```



