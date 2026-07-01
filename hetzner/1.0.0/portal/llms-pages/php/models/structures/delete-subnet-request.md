# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q


# Class Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipRange` | `string` | Required | IP range of subnet to delete | getIpRange(): string | setIpRange(string ipRange): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\DeleteSubnetRequestBuilder;

$deleteSubnetRequest = DeleteSubnetRequestBuilder::init(
    '10.0.1.0/24'
)->build();
```



