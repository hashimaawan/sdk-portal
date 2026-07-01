# Create Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`CreateCertificateResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/nullable-action.md) | Optional | - | NullableAction getAction() | setAction(NullableAction action) |
| `Certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/certificate.md) | Required | - | Certificate getCertificate() | setCertificate(Certificate certificate) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Certificate;
import cloud.hetzner.api.models.CreateCertificateResponse;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Issuance;
import cloud.hetzner.api.models.NullableAction;
import cloud.hetzner.api.models.Renewal;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.Status;
import cloud.hetzner.api.models.Status2;
import cloud.hetzner.api.models.Type;
import cloud.hetzner.api.models.UsedBy;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

CreateCertificateResponse createCertificateResponse = new CreateCertificateResponse.Builder(
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
            put("key0", "labels8");
            put("key1", "labels7");
            put("key2", "labels6");
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
.action(new NullableAction.Builder(
        "command6",
        new Error.Builder(
            "code2",
            "message4"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "finished0",
        238,
        143.26D,
        Arrays.asList(
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        "started8",
        Status.RUNNING
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



