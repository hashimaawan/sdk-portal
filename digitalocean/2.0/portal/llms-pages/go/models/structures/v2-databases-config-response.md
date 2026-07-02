# V2 Databases Config Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMENvbmZpZyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesConfigResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Config` | [`models.V2DatabasesConfigResponseConfig`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/v2-databases-config-response-config.md) | Required | This is a container for any-of cases. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DatabasesConfigResponse := models.V2DatabasesConfigResponse{
        Config:                models.V2DatabasesConfigResponseConfigContainer.FromConfig(models.Config{
            BackupHour:                   models.ToPointer(3),
            BackupMinute:                 models.ToPointer(30),
            BinlogRetentionPeriod:        models.ToPointer(float64(600)),
            ConnectTimeout:               models.ToPointer(10),
            DefaultTimeZone:              models.ToPointer("+03:00"),
            GroupConcatMaxLen:            models.ToPointer(1024),
            InformationSchemaStatsExpiry: models.ToPointer(86400),
            InnodbFtMinTokenSize:         models.ToPointer(3),
            InnodbFtServerStopwordTable:  models.ToPointer("db_name/table_name"),
            InnodbLockWaitTimeout:        models.ToPointer(50),
            InnodbLogBufferSize:          models.ToPointer(16777216),
            InnodbOnlineAlterLogMaxSize:  models.ToPointer(134217728),
            InnodbPrintAllDeadlocks:      models.ToPointer(true),
            InnodbRollbackOnTimeout:      models.ToPointer(true),
            InteractiveTimeout:           models.ToPointer(3600),
            InternalTmpMemStorageEngine:  models.ToPointer(models.InternalTmpMemStorageEngine_Temptable),
            LongQueryTime:                models.ToPointer(float64(10)),
            MaxAllowedPacket:             models.ToPointer(67108864),
            MaxHeapTableSize:             models.ToPointer(16777216),
            NetReadTimeout:               models.ToPointer(30),
            NetWriteTimeout:              models.ToPointer(30),
            SlowQueryLog:                 models.ToPointer(true),
            SortBufferSize:               models.ToPointer(262144),
            SqlMode:                      models.ToPointer("ANSI,TRADITIONAL"),
            SqlRequirePrimaryKey:         models.ToPointer(true),
            TmpTableSize:                 models.ToPointer(16777216),
            WaitTimeout:                  models.ToPointer(28800),
            AdditionalProperties:         map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



