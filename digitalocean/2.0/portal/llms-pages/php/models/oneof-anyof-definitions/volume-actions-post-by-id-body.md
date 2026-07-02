# Volume Actions Post by Id Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZUFjdGlvbnNQb3N0QnlJZEJvZHk


# Data Type

`V2VolumesActionsRequest|V2VolumesActionsRequest1|V2VolumesActionsRequest2`


# Cases

| Type |
|  --- |
| [`V2VolumesActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-volumes-actions-request.md) |
| [`V2VolumesActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-volumes-actions-request-1.md) |
| [`V2VolumesActionsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-volumes-actions-request-2.md) |


# V2VolumesActionsRequest

## Initialization Code

### Example

```php
$value = V2VolumesActionsRequestBuilder::init(
    Type21::ATTACH,
    11612190
)
    ->region(Region2::NYC3)
    ->tags(
        [
            'base-image',
            'prod'
        ]
    )
    ->build();
```


# V2VolumesActionsRequest1

## Initialization Code

### Example

```php
$value = V2VolumesActionsRequest1Builder::init(
    Type21::ATTACH,
    11612190
)
    ->region(Region2::NYC3)
    ->build();
```


# V2VolumesActionsRequest2

## Initialization Code

### Example

```php
$value = V2VolumesActionsRequest2Builder::init(
    Type21::ATTACH,
    15384
)
    ->region(Region2::NYC3)
    ->build();
```



