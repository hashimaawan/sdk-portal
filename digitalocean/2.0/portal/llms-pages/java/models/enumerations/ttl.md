# Ttl

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlR0bA

The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.


# Enum Type Name

`Ttl`


# Fields

| Name |
|  --- |
| `ENUM_60` |
| `ENUM_600` |
| `ENUM_3600` |
| `ENUM_86400` |
| `ENUM_604800` |


# Example

```java
import com.digitalocean.api.models.Ttl;

Ttl ttl = Ttl.ENUM_60;
```



