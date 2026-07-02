# Volume Actions Post by Id Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZUFjdGlvbnNQb3N0QnlJZEJvZHk


# Class Name

`VolumeActionsPostByIdBody`


# Cases

| Type |
|  --- |
| [`V2VolumesActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-volumes-actions-request.md) |
| [`V2VolumesActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-volumes-actions-request-1.md) |
| [`V2VolumesActionsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-volumes-actions-request-2.md) |


# V2VolumesActionsRequest

## Initialization Code

### Example

```ts
const value: VolumeActionsPostByIdBody = {
  type: Type21.Attach,
  dropletId: 11612190,
  region: Region2.Nyc3,
  tags: [
    'base-image',
    'prod'
  ],
};
```


# V2VolumesActionsRequest1

## Initialization Code

### Example

```ts
const value: VolumeActionsPostByIdBody = {
  type: Type21.Attach,
  dropletId: 11612190,
  region: Region2.Nyc3,
};
```


# V2VolumesActionsRequest2

## Initialization Code

### Example

```ts
const value: VolumeActionsPostByIdBody = {
  type: Type21.Attach,
  sizeGigabytes: 15384,
  region: Region2.Nyc3,
};
```



