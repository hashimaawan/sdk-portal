# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q


# Class Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `automount` | `?bool` | Optional | Auto-mount the Volume after attaching it | getAutomount(): ?bool | setAutomount(?bool automount): void |
| `server` | `int` | Required | ID of the Server the Volume will be attached to | getServer(): int | setServer(int server): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\AttachVolumeRequestBuilder;

$attachVolumeRequest = AttachVolumeRequestBuilder::init(
    43
)
    ->automount(false)
    ->build();
```



