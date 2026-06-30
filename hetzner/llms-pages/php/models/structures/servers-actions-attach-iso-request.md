# Servers Actions Attach Iso Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEF0dGFjaCUyNTIwSXNvJTI1MjBSZXF1ZXN0


# Class Name

`ServersActionsAttachIsoRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `iso` | `string` | Required | ID or name of ISO to attach to the Server as listed in GET `/isos` | getIso(): string | setIso(string iso): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServersActionsAttachIsoRequestBuilder;

$serversActionsAttachIsoRequest = ServersActionsAttachIsoRequestBuilder::init(
    'FreeBSD-11.0-RELEASE-amd64-dvd1'
)->build();
```



