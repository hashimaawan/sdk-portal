# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0


# Class Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | [`?Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) | getLabels(): ?Labels2 | setLabels(?Labels2 labels): void |
| `name` | `?string` | Optional | New network name | getName(): ?string | setName(?string name): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\UpdateNetworkRequestBuilder;
use HetznerCloudAPILib\Models\Builders\Labels2Builder;

$updateNetworkRequest = UpdateNetworkRequestBuilder::init()
    ->labels(
        Labels2Builder::init()
            ->labelkey('labelkey4')
            ->build()
    )
    ->name('new-name')
    ->build();
```



