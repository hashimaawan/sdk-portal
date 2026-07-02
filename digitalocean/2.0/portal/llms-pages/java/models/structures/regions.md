# Regions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlZ2lvbnM

A map of region to regional state

*This model accepts additional fields of type Object.*


# Class Name

`Regions`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EuWest` | [`EuWest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/eu-west.md) | Optional | - | EuWest getEuWest() | setEuWest(EuWest euWest) |
| `UsEast` | [`EuWest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/eu-west.md) | Optional | - | EuWest getUsEast() | setUsEast(EuWest usEast) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.EuWest;
import com.digitalocean.api.models.Regions;
import com.digitalocean.api.models.Status16;
import java.io.IOException;

Regions regions = new Regions.Builder()
    .euWest(new EuWest.Builder()
        .status(Status16.DOWN)
        .statusChangedAt("status_changed_at4")
        .thirtyDayUptimePercentage(227.78D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .usEast(new EuWest.Builder()
        .status(Status16.DOWN)
        .statusChangedAt("status_changed_at4")
        .thirtyDayUptimePercentage(121.56D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



