# Purpose

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlB1cnBvc2U

Some item types, Login and Password, have fields used for autofill. This property indicates that purpose and is required for some item types.


# Enum Type Name

`Purpose`


# Fields

| Name |
|  --- |
| `USERNAME` |
| `PASSWORD` |
| `NOTES` |


# Example

```php
use M1PasswordConnectLib\Models\Purpose;

$purpose = Purpose::PASSWORD;
```



