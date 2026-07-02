# Status 15

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXR1czE1

The current status of this garbage collection.


# Enum Type Name

`Status15`


# Fields

| Name |
|  --- |
| `Requested` |
| `EnumWaitingForWriteJwTsToExpire` |
| `EnumScanningManifests` |
| `EnumDeletingUnreferencedBlobs` |
| `Cancelling` |
| `Failed` |
| `Succeeded` |
| `Cancelled` |


# Example

```csharp
using DigitalOceanApi.Standard.Models;

Status15 status15 = Status15.Cancelling;
```



