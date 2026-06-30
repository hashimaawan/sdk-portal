# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA


# Class Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | Description of the Image, will be auto-generated if not set | getDescription(): ?string | setDescription(?string description): void |
| `labels` | [`?Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) | getLabels(): ?Labels | setLabels(?Labels labels): void |
| `type` | [`?string(Type63Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) | getType(): ?string | setType(?string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreateImageRequestBuilder;
use HetznerCloudAPILib\Models\Builders\LabelsBuilder;
use HetznerCloudAPILib\Models\Type63Enum;

$createImageRequest = CreateImageRequestBuilder::init()
    ->description('my image')
    ->labels(
        LabelsBuilder::init()
            ->labelkey('labelkey4')
            ->build()
    )
    ->type(Type63Enum::SNAPSHOT)
    ->build();
```



