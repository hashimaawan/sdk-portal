# Ttl

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlR0bA

The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.


# Enum Type Name

`Ttl`


# Fields

| Name |
|  --- |
| `Enum60` |
| `Enum600` |
| `Enum3600` |
| `Enum86400` |
| `Enum604800` |


# Example

```ts
import { Ttl } from 'digitalocean-apilib';

const ttl = Ttl.Enum60;
```



