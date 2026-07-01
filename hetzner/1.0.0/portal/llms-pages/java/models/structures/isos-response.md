# Isos Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`IsosResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Isos` | [`List<Iso>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/iso.md) | Required | - | List<Iso> getIsos() | setIsos(List<Iso> isos) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Iso;
import cloud.hetzner.api.models.IsosResponse;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.Type26;
import java.io.IOException;
import java.util.Arrays;

IsosResponse isosResponse = new IsosResponse.Builder(
    Arrays.asList(
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
)
.meta(new Meta.Builder(
        new Pagination.Builder(
            77.7D,
            209.18D,
            17.58D,
            13.34D,
            50.02D,
            206.64D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



