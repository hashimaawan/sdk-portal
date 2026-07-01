# Datacenters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`DatacentersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Datacenters` | [`List<Datacenter>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/datacenter.md) | Required | - | List<Datacenter> getDatacenters() | setDatacenters(List<Datacenter> datacenters) |
| `Recommendation` | `double` | Required | The Datacenter which is recommended to be used to create new Servers. | double getRecommendation() | setRecommendation(double recommendation) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Datacenter;
import cloud.hetzner.api.models.DatacentersResponse;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.ServerTypes;
import java.io.IOException;
import java.util.Arrays;

DatacentersResponse datacentersResponse = new DatacentersResponse.Builder(
    Arrays.asList(
        new Datacenter.Builder(
            "Falkenstein DC Park 8",
            42,
            new Location.Builder(
                "Falkenstein",
                "DE",
                "Falkenstein DC Park 1",
                1D,
                50.47612D,
                12.370071D,
                "fsn1",
                "eu-central"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            "fsn1-dc8",
            new ServerTypes.Builder(
                Arrays.asList(
                    1D,
                    2D,
                    3D
                ),
                Arrays.asList(
                    1D,
                    2D,
                    3D
                ),
                Arrays.asList(
                    1D,
                    2D,
                    3D
                )
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    1D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



