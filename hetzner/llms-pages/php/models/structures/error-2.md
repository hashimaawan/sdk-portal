# Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkVycm9yMg

If issuance or renewal reports `failed`, this property contains information about what happened


# Class Name

`Error2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `code` | `?string` | Optional | - | getCode(): ?string | setCode(?string code): void |
| `message` | `?string` | Optional | - | getMessage(): ?string | setMessage(?string message): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Error2Builder;

$error2 = Error2Builder::init()
    ->code('code2')
    ->message('message4')
    ->build();
```



