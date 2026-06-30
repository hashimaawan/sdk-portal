# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkVycm9y

Error message for the Action if error occurred, otherwise null


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `code` | `string` | Required | Fixed machine readable code | getCode(): string | setCode(string code): void |
| `message` | `string` | Required | Humanized error message | getMessage(): string | setMessage(string message): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;

$error = ErrorBuilder::init(
    'action_failed',
    'Action failed'
)->build();
```



