# Single Droplet Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlNpbmdsZSUyNTIwRHJvcGxldCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`SingleDropletResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Droplet` | [`Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/droplet.md) | Required | - | Droplet getDroplet() | setDroplet(Droplet droplet) |
| `Links` | [`Links1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links-1.md) | Required | - | Links1 getLinks() | setLinks(Links1 links) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Action1;
import com.digitalocean.api.models.Distribution;
import com.digitalocean.api.models.Droplet;
import com.digitalocean.api.models.Image1;
import com.digitalocean.api.models.Kernel;
import com.digitalocean.api.models.Links1;
import com.digitalocean.api.models.Networks;
import com.digitalocean.api.models.NextBackupWindow;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.Region2;
import com.digitalocean.api.models.SingleDropletResponse;
import com.digitalocean.api.models.Size;
import com.digitalocean.api.models.Status7;
import com.digitalocean.api.models.Status8;
import com.digitalocean.api.models.Type10;
import com.digitalocean.api.models.Type11;
import com.digitalocean.api.models.Type9;
import com.digitalocean.api.models.V4;
import com.digitalocean.api.models.V6;
import java.io.IOException;
import java.util.Arrays;

SingleDropletResponse singleDropletResponse = new SingleDropletResponse.Builder(
    new Droplet.Builder(
        Arrays.asList(
            53893572
        ),
        DateTimeHelper.fromRfc8601DateTime("2020-07-21T18:37:44Z"),
        25,
        Arrays.asList(
            "backups",
            "private_networking",
            "ipv6"
        ),
        3164444,
        new Image1.Builder()
            .createdAt(DateTimeHelper.fromRfc8601DateTime("2020-05-04T22:23:02Z"))
            .description("description6")
            .distribution(Distribution.UBUNTU)
            .errorMessage("error_message8")
            .id(7555620)
            .minDiskSize(20)
            .name("Nifty New Snapshot")
            .mPublic(true)
            .regions(Arrays.asList(
                Region2.NYC1,
                Region2.NYC2
            ))
            .sizeGigabytes(2.34D)
            .slug("nifty1")
            .status(Status7.NEW)
            .tags(Arrays.asList(
                "base-image",
                "prod"
            ))
            .type(Type9.SNAPSHOT)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        false,
        1024,
        "example.com",
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
            .end(DateTimeHelper.fromRfc8601DateTime("2019-12-04T23:00:00Z"))
            .start(DateTimeHelper.fromRfc8601DateTime("2019-12-04T00:00:00Z"))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Region.Builder(
            true,
            Arrays.asList(
                "private_networking",
                "backups",
                "ipv6",
                "metadata",
                "install_agent",
                "storage",
                "image_transfer"
            ),
            "New York 3",
            Arrays.asList(
                "s-1vcpu-1gb",
                "s-1vcpu-2gb",
                "s-1vcpu-3gb",
                "s-2vcpu-2gb",
                "s-3vcpu-1gb",
                "s-2vcpu-4gb",
                "s-4vcpu-8gb",
                "s-6vcpu-16gb",
                "s-8vcpu-32gb",
                "s-12vcpu-48gb",
                "s-16vcpu-64gb",
                "s-20vcpu-96gb",
                "s-24vcpu-128gb",
                "s-32vcpu-192g"
            ),
            "nyc3"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Size.Builder(
            true,
            "Basic",
            25,
            1024,
            0.00743999984115362D,
            5D,
            Arrays.asList(
                "ams2",
                "ams3",
                "blr1",
                "fra1",
                "lon1",
                "nyc1",
                "nyc2",
                "nyc3",
                "sfo1",
                "sfo2",
                "sfo3",
                "sgp1",
                "tor1"
            ),
            "s-1vcpu-1gb",
            1D,
            1
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "s-1vcpu-1gb",
        Arrays.asList(
            67512819
        ),
        Status8.ACTIVE,
        Arrays.asList(
            "web",
            "env:prod"
        ),
        1,
        Arrays.asList(
            "506f78a4-e098-11e5-ad9f-000f53306ae1"
        )
    )
    .kernel(new Kernel.Builder()
            .id(16)
            .name("name4")
            .version("version0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .vpcUuid("760e09ef-dc84-11e8-981e-3cfdfeaae000")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    new Links1.Builder()
        .actions(Arrays.asList(
            new Action1.Builder()
                .href("href0")
                .id(154)
                .rel("rel4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



