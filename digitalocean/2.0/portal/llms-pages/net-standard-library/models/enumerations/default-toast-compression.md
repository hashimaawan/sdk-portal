# Default Toast Compression

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRlZmF1bHRUb2FzdENvbXByZXNzaW9u

Specifies the default TOAST compression method for values of compressible columns (the default is lz4).


# Enum Type Name

`DefaultToastCompression`


# Fields

| Name |
|  --- |
| `Lz4` |
| `Pglz` |


# Example

```csharp
using DigitalOceanApi.Standard.Models;

DefaultToastCompression defaultToastCompression = DefaultToastCompression.Lz4;
```



