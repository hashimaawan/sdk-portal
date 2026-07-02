# Mysql

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk15c3Fs

*This model accepts additional fields of type Object.*


# Class Name

`Mysql`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Regions` | `List<String>` | Optional, Read-only | An array of strings containing the names of available regions | List<String> getRegions() | setRegions(List<String> regions) |
| `Versions` | `List<String>` | Optional, Read-only | An array of strings containing the names of available regions | List<String> getVersions() | setVersions(List<String> versions) |
| `Layouts` | [`List<Layout>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/layout.md) | Optional, Read-only | An array of objects, each indicating the node sizes (otherwise referred to as slugs) that are available with various numbers of nodes in the database cluster. Each slugs denotes the node's identifier, CPU, and RAM (in that order). | List<Layout> getLayouts() | setLayouts(List<Layout> layouts) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Layout;
import com.digitalocean.api.models.Mysql;
import java.io.IOException;
import java.util.Arrays;

Mysql mysql = new Mysql.Builder()
    .regions(Arrays.asList(
        "ams3",
        "blr1"
    ))
    .versions(Arrays.asList(
        "4.4",
        "5.0"
    ))
    .layouts(Arrays.asList(
        new Layout.Builder()
            .numNodes(190)
            .sizes(Arrays.asList(
                "sizes2",
                "sizes3"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Layout.Builder()
            .numNodes(190)
            .sizes(Arrays.asList(
                "sizes2",
                "sizes3"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Layout.Builder()
            .numNodes(190)
            .sizes(Arrays.asList(
                "sizes2",
                "sizes3"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



