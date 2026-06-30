# Assign Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkFzc2lnbkZsb2F0aW5nSVBSZXF1ZXN0

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `floating_ip_assigned`        | The floating IP is already assigned                           |


# Class Name

`AssignFloatingIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `server` | `int` | Required | ID of the Server the Floating IP shall be assigned to | getServer(): int | setServer(int server): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\AssignFloatingIPRequestBuilder;

$assignFloatingIPRequest = AssignFloatingIPRequestBuilder::init(
    42
)->build();
```



