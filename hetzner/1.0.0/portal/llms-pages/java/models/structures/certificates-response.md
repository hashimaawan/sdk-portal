# Certificates Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlc1Jlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`CertificatesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Certificates` | [`List<Certificate>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/certificate.md) | Required | - | List<Certificate> getCertificates() | setCertificates(List<Certificate> certificates) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Certificate;
import cloud.hetzner.api.models.CertificatesResponse;
import cloud.hetzner.api.models.Issuance;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.Renewal;
import cloud.hetzner.api.models.Status2;
import cloud.hetzner.api.models.Type;
import cloud.hetzner.api.models.UsedBy;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

CertificatesResponse certificatesResponse = new CertificatesResponse.Builder(
    Arrays.asList(
        new Certificate.Builder(
            "-----BEGIN CERTIFICATE-----\n...",
            "2016-01-30T23:55:00+00:00",
            Arrays.asList(
                "example.com",
                "webmail.example.com",
                "www.example.com"
            ),
            "03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f",
            42,
            new LinkedHashMap<String, String>() {{
                put("key0", "labels2");
                put("key1", "labels1");
                put("key2", "labels0");
            }},
            "my-resource",
            "2019-07-08T09:59:59+00:00",
            "2019-01-08T10:00:00+00:00",
            Arrays.asList(
                new UsedBy.Builder(
                    4711,
                    "load_balancer"
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            )
        )
        .status(new Status2.Builder()
                .error(null)
                .issuance(Issuance.COMPLETED)
                .renewal(Renewal.FAILED)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .type(Type.UPLOADED)
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



