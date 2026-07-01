# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/iso.md) | Required | - | Iso getIso() | setIso(Iso iso) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Iso;
import cloud.hetzner.api.models.IsosResponse1;
import cloud.hetzner.api.models.Type26;
import java.io.IOException;

IsosResponse1 isosResponse1 = new IsosResponse1.Builder(
    new Iso.Builder(
        "2018-02-28T00:00:00+00:00",
        "FreeBSD 11.0 x64",
        42,
        "FreeBSD-11.0-RELEASE-amd64-dvd1",
        Type26.ENUM_PUBLIC
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



