# Image Actions Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkltYWdlQWN0aW9uc1Bvc3RCb2R5


# Class Name

`ImageActionsPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.V2ImagesActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-images-actions-request.md) | models.ImageActionsPostBodyContainer.FromV2ImagesActionsRequest(models.V2ImagesActionsRequest v2ImagesActionsRequest) |
| [`models.V2ImagesActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-images-actions-request-1.md) | models.ImageActionsPostBodyContainer.FromV2ImagesActionsRequest1(models.V2ImagesActionsRequest1 v2ImagesActionsRequest1) |


# models.V2ImagesActionsRequest

## Initialization Code

### Example

```go
value := models.ImageActionsPostBodyContainer.FromV2ImagesActionsRequest(models.V2ImagesActionsRequest{
    Type:                  models.Type15_Convert,
})
```


# models.V2ImagesActionsRequest1

## Initialization Code

### Example

```go
value := models.ImageActionsPostBodyContainer.FromV2ImagesActionsRequest1(models.V2ImagesActionsRequest1{
    Type:                  models.Type15_Convert,
    Region:                models.Region2_Nyc3,
})
```



