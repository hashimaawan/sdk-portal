# Auth Plugin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkF1dGhQbHVnaW4

A string specifying the authentication method to be used for connections
to the MySQL user account. The valid values are `mysql_native_password`
or `caching_sha2_password`. If excluded when creating a new user, the
default for the version of MySQL in use will be used. As of MySQL 8.0, the
default is `caching_sha2_password`.


# Enum Type Name

`AuthPlugin`


# Fields

| Name |
|  --- |
| `MYSQL_NATIVE_PASSWORD` |
| `CACHING_SHA2_PASSWORD` |


# Example

```php
use DigitalOceanApiLib\Models\AuthPlugin;

$authPlugin = AuthPlugin::MYSQL_NATIVE_PASSWORD;
```



