# Image Actions Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkltYWdlQWN0aW9uc1Bvc3RCb2R5


# Class Name

`ImageActionsPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2ImagesActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-images-actions-request.md) | ImageActionsPostBody.fromV2ImagesActionsRequest(V2ImagesActionsRequest v2ImagesActionsRequest) |
| [`V2ImagesActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-images-actions-request-1.md) | ImageActionsPostBody.fromV2ImagesActionsRequest1(V2ImagesActionsRequest1 v2ImagesActionsRequest1) |


# V2ImagesActionsRequest

## Initialization Code

### Example

```java
ImageActionsPostBody.fromV2ImagesActionsRequest(
        new V2ImagesActionsRequest.Builder(
            Type15.CONVERT
        )
        .build()
    )
```


# V2ImagesActionsRequest1

## Initialization Code

### Example

```java
ImageActionsPostBody.fromV2ImagesActionsRequest1(
        new V2ImagesActionsRequest1.Builder(
            Type15.CONVERT,
            Region2.NYC3
        )
        .build()
    )
```



