# Timescaledb

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlRpbWVzY2FsZWRi

TimescaleDB extension configuration values

*This model accepts additional fields of type Object.*


# Class Name

`Timescaledb`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MaxBackgroundWorkers` | `Integer` | Optional | The number of background workers for timescaledb operations.  Set to the sum of your number of databases and the total number of concurrent background workers you want running at any given point in time.<br><br>**Constraints**: `>= 1`, `<= 4096` | Integer getMaxBackgroundWorkers() | setMaxBackgroundWorkers(Integer maxBackgroundWorkers) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Timescaledb;
import java.io.IOException;

Timescaledb timescaledb = new Timescaledb.Builder()
    .maxBackgroundWorkers(8)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



