# V2 Monitoring Metrics Droplet Bandwidth Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBNZXRyaWNzJTI1MjBEcm9wbGV0JTI1MjBCYW5kd2lkdGglMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2MonitoringMetricsDropletBandwidthResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`Data`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/data.md) | Required | - | Data getData() | setData(Data data) |
| `Status` | [`Status13`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-13.md) | Required | - | Status13 getStatus() | setStatus(Status13 status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Data;
import com.digitalocean.api.models.Result;
import com.digitalocean.api.models.Status13;
import com.digitalocean.api.models.V2MonitoringMetricsDropletBandwidthResponse;
import com.digitalocean.api.models.containers.ResultValues;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

V2MonitoringMetricsDropletBandwidthResponse v2MonitoringMetricsDropletBandwidthResponse = new V2MonitoringMetricsDropletBandwidthResponse.Builder(
    new Data.Builder(
        Arrays.asList(
            new Result.Builder(
                new LinkedHashMap<String, String>() {{
                    put("host_id", "19201920");
                }},
                Arrays.asList(
                    Arrays.asList(
                        ResultValues.fromNumber(
                            1435781430
                        ),
                        ResultValues.fromString(
                            "1"
                        )
                    ),
                    Arrays.asList(
                        ResultValues.fromNumber(
                            1435781445
                        ),
                        ResultValues.fromString(
                            "1"
                        )
                    )
                )
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        "matrix"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    Status13.SUCCESS
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



