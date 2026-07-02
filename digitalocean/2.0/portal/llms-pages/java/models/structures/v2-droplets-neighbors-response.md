# V2 Droplets Neighbors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwTmVpZ2hib3JzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2DropletsNeighborsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Droplets` | [`List<Droplet>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/droplet.md) | Optional | - | List<Droplet> getDroplets() | setDroplets(List<Droplet> droplets) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Distribution;
import com.digitalocean.api.models.Droplet;
import com.digitalocean.api.models.Image1;
import com.digitalocean.api.models.Kernel;
import com.digitalocean.api.models.Networks;
import com.digitalocean.api.models.NextBackupWindow;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.Size;
import com.digitalocean.api.models.Status8;
import com.digitalocean.api.models.Type10;
import com.digitalocean.api.models.Type11;
import com.digitalocean.api.models.V2DropletsNeighborsResponse;
import com.digitalocean.api.models.V4;
import com.digitalocean.api.models.V6;
import java.io.IOException;
import java.util.Arrays;

V2DropletsNeighborsResponse v2DropletsNeighborsResponse = new V2DropletsNeighborsResponse.Builder()
    .droplets(Arrays.asList(
        new Droplet.Builder(
            Arrays.asList(
                104,
                105
            ),
            DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
            98,
            Arrays.asList(
                "features1",
                "features2",
                "features3"
            ),
            232,
            new Image1.Builder()
                .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .description("description6")
                .distribution(Distribution.COREOS)
                .errorMessage("error_message8")
                .id(128)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            false,
            16,
            "name0",
            new Networks.Builder()
                .v4(Arrays.asList(
                    new V4.Builder()
                        .gateway("gateway2")
                        .ipAddress("ip_address2")
                        .netmask("netmask2")
                        .type(Type10.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new V4.Builder()
                        .gateway("gateway2")
                        .ipAddress("ip_address2")
                        .netmask("netmask2")
                        .type(Type10.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new V4.Builder()
                        .gateway("gateway2")
                        .ipAddress("ip_address2")
                        .netmask("netmask2")
                        .type(Type10.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
                .v6(Arrays.asList(
                    new V6.Builder()
                        .gateway("gateway4")
                        .ipAddress("ip_address4")
                        .netmask(106)
                        .type(Type11.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new V6.Builder()
                        .gateway("gateway4")
                        .ipAddress("ip_address4")
                        .netmask(106)
                        .type(Type11.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new NextBackupWindow.Builder()
                .end(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .start(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Region.Builder(
                false,
                Arrays.asList(
                    "features7",
                    "features8",
                    "features9"
                ),
                "name6",
                Arrays.asList(
                    "sizes6"
                ),
                "slug0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Size.Builder(
                false,
                "description0",
                252,
                168,
                121.04D,
                162.04D,
                Arrays.asList(
                    "regions5"
                ),
                "slug6",
                150.78D,
                234
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            "size_slug0",
            Arrays.asList(
                93,
                94
            ),
            Status8.ENUM_NEW,
            Arrays.asList(
                "tags5"
            ),
            80,
            Arrays.asList(
                "volume_ids0",
                "volume_ids1",
                "volume_ids2"
            )
        )
        .kernel(new Kernel.Builder()
                .id(16)
                .name("name4")
                .version("version0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .vpcUuid("vpc_uuid0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Droplet.Builder(
            Arrays.asList(
                104,
                105
            ),
            DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
            98,
            Arrays.asList(
                "features1",
                "features2",
                "features3"
            ),
            232,
            new Image1.Builder()
                .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .description("description6")
                .distribution(Distribution.COREOS)
                .errorMessage("error_message8")
                .id(128)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            false,
            16,
            "name0",
            new Networks.Builder()
                .v4(Arrays.asList(
                    new V4.Builder()
                        .gateway("gateway2")
                        .ipAddress("ip_address2")
                        .netmask("netmask2")
                        .type(Type10.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new V4.Builder()
                        .gateway("gateway2")
                        .ipAddress("ip_address2")
                        .netmask("netmask2")
                        .type(Type10.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new V4.Builder()
                        .gateway("gateway2")
                        .ipAddress("ip_address2")
                        .netmask("netmask2")
                        .type(Type10.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
                .v6(Arrays.asList(
                    new V6.Builder()
                        .gateway("gateway4")
                        .ipAddress("ip_address4")
                        .netmask(106)
                        .type(Type11.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new V6.Builder()
                        .gateway("gateway4")
                        .ipAddress("ip_address4")
                        .netmask(106)
                        .type(Type11.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new NextBackupWindow.Builder()
                .end(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .start(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Region.Builder(
                false,
                Arrays.asList(
                    "features7",
                    "features8",
                    "features9"
                ),
                "name6",
                Arrays.asList(
                    "sizes6"
                ),
                "slug0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Size.Builder(
                false,
                "description0",
                252,
                168,
                121.04D,
                162.04D,
                Arrays.asList(
                    "regions5"
                ),
                "slug6",
                150.78D,
                234
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            "size_slug0",
            Arrays.asList(
                93,
                94
            ),
            Status8.ENUM_NEW,
            Arrays.asList(
                "tags5"
            ),
            80,
            Arrays.asList(
                "volume_ids0",
                "volume_ids1",
                "volume_ids2"
            )
        )
        .kernel(new Kernel.Builder()
                .id(16)
                .name("name4")
                .version("version0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .vpcUuid("vpc_uuid0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Droplet.Builder(
            Arrays.asList(
                104,
                105
            ),
            DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
            98,
            Arrays.asList(
                "features1",
                "features2",
                "features3"
            ),
            232,
            new Image1.Builder()
                .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .description("description6")
                .distribution(Distribution.COREOS)
                .errorMessage("error_message8")
                .id(128)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            false,
            16,
            "name0",
            new Networks.Builder()
                .v4(Arrays.asList(
                    new V4.Builder()
                        .gateway("gateway2")
                        .ipAddress("ip_address2")
                        .netmask("netmask2")
                        .type(Type10.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new V4.Builder()
                        .gateway("gateway2")
                        .ipAddress("ip_address2")
                        .netmask("netmask2")
                        .type(Type10.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new V4.Builder()
                        .gateway("gateway2")
                        .ipAddress("ip_address2")
                        .netmask("netmask2")
                        .type(Type10.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
                .v6(Arrays.asList(
                    new V6.Builder()
                        .gateway("gateway4")
                        .ipAddress("ip_address4")
                        .netmask(106)
                        .type(Type11.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new V6.Builder()
                        .gateway("gateway4")
                        .ipAddress("ip_address4")
                        .netmask(106)
                        .type(Type11.ENUM_PUBLIC)
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new NextBackupWindow.Builder()
                .end(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .start(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Region.Builder(
                false,
                Arrays.asList(
                    "features7",
                    "features8",
                    "features9"
                ),
                "name6",
                Arrays.asList(
                    "sizes6"
                ),
                "slug0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Size.Builder(
                false,
                "description0",
                252,
                168,
                121.04D,
                162.04D,
                Arrays.asList(
                    "regions5"
                ),
                "slug6",
                150.78D,
                234
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            "size_slug0",
            Arrays.asList(
                93,
                94
            ),
            Status8.ENUM_NEW,
            Arrays.asList(
                "tags5"
            ),
            80,
            Arrays.asList(
                "volume_ids0",
                "volume_ids1",
                "volume_ids2"
            )
        )
        .kernel(new Kernel.Builder()
                .id(16)
                .name("name4")
                .version("version0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .vpcUuid("vpc_uuid0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



