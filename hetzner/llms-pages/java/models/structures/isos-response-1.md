# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/iso.md) | Required | - | Iso getIso() | setIso(Iso iso) |


# Example

```java
import cloud.hetzner.api.models.Iso;
import cloud.hetzner.api.models.IsosResponse1;
import cloud.hetzner.api.models.Type26Enum;

IsosResponse1 isosResponse1 = new IsosResponse1.Builder(
    new Iso.Builder(
        "2018-02-28T00:00:00+00:00",
        "FreeBSD 11.0 x64",
        42,
        "FreeBSD-11.0-RELEASE-amd64-dvd1",
        Type26Enum.ENUM_PUBLIC
    )
    .build()
)
.build();
```



