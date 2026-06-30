# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0


# Class Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sshKeys` | `?(int[])` | Optional | Array of SSH key IDs which should be injected into the rescue system. | getSshKeys(): ?array | setSshKeys(?array sshKeys): void |
| `type` | [`?string(Type65Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) | getType(): ?string | setType(?string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServersActionsEnableRescueRequestBuilder;
use HetznerCloudAPILib\Models\Type65Enum;

$serversActionsEnableRescueRequest = ServersActionsEnableRescueRequestBuilder::init()
    ->sshKeys(
        [
            2323
        ]
    )
    ->type(Type65Enum::LINUX64)
    ->build();
```



