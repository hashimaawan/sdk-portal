# V2 Databases Config Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMENvbmZpZyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesConfigResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Config` | [`V2DatabasesConfigResponseConfig`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/v2-databases-config-response-config.md) | Required | This is a container for any-of cases. | V2DatabasesConfigResponseConfig getConfig() | setConfig(V2DatabasesConfigResponseConfig config) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Config;
import com.digitalocean.api.models.InternalTmpMemStorageEngine;
import com.digitalocean.api.models.V2DatabasesConfigResponse;
import com.digitalocean.api.models.containers.V2DatabasesConfigResponseConfig;
import java.io.IOException;

V2DatabasesConfigResponse v2DatabasesConfigResponse = new V2DatabasesConfigResponse.Builder(
    V2DatabasesConfigResponseConfig.fromConfig(
        new Config.Builder()
            .backupHour(3)
            .backupMinute(30)
            .binlogRetentionPeriod(600D)
            .connectTimeout(10)
            .defaultTimeZone("+03:00")
            .groupConcatMaxLen(1024)
            .informationSchemaStatsExpiry(86400)
            .innodbFtMinTokenSize(3)
            .innodbFtServerStopwordTable("db_name/table_name")
            .innodbLockWaitTimeout(50)
            .innodbLogBufferSize(16777216)
            .innodbOnlineAlterLogMaxSize(134217728)
            .innodbPrintAllDeadlocks(true)
            .innodbRollbackOnTimeout(true)
            .interactiveTimeout(3600)
            .internalTmpMemStorageEngine(InternalTmpMemStorageEngine.TEMPTABLE)
            .longQueryTime(10D)
            .maxAllowedPacket(67108864)
            .maxHeapTableSize(16777216)
            .netReadTimeout(30)
            .netWriteTimeout(30)
            .slowQueryLog(true)
            .sortBufferSize(262144)
            .sqlMode("ANSI,TRADITIONAL")
            .sqlRequirePrimaryKey(true)
            .tmpTableSize(16777216)
            .waitTimeout(28800)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



