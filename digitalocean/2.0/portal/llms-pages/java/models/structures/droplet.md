# Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRyb3BsZXQ

*This model accepts additional fields of type Object.*


# Class Name

`Droplet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BackupIds` | `List<Integer>` | Required | An array of backup IDs of any backups that have been taken of the Droplet instance.  Droplet backups are enabled at the time of the instance creation. | List<Integer> getBackupIds() | setBackupIds(List<Integer> backupIds) |
| `CreatedAt` | `LocalDateTime` | Required | A time value given in ISO8601 combined date and time format that represents when the Droplet was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Disk` | `int` | Required | The size of the Droplet's disk in gigabytes. | int getDisk() | setDisk(int disk) |
| `Features` | `List<String>` | Required | An array of features enabled on this Droplet. | List<String> getFeatures() | setFeatures(List<String> features) |
| `Id` | `int` | Required | A unique identifier for each Droplet instance. This is automatically generated upon Droplet creation. | int getId() | setId(int id) |
| `Image` | [`Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/image-1.md) | Required | - | Image1 getImage() | setImage(Image1 image) |
| `Kernel` | [`Kernel`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/kernel.md) | Optional | **Note**: All Droplets created after March 2017 use internal kernels by default.<br>These Droplets will have this attribute set to `null`.<br><br>The current [kernel](https://www.digitalocean.com/docs/droplets/how-to/kernel/)<br>for Droplets with externally managed kernels. This will initially be set to<br>the kernel of the base image when the Droplet is created. | Kernel getKernel() | setKernel(Kernel kernel) |
| `Locked` | `boolean` | Required | A boolean value indicating whether the Droplet has been locked, preventing actions by users. | boolean getLocked() | setLocked(boolean locked) |
| `Memory` | `int` | Required | Memory of the Droplet in megabytes.<br><br>**Constraints**: *Multiple Of*: `8` | int getMemory() | setMemory(int memory) |
| `Name` | `String` | Required | The human-readable name set for the Droplet instance. | String getName() | setName(String name) |
| `Networks` | [`Networks`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/networks.md) | Required | The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is. | Networks getNetworks() | setNetworks(Networks networks) |
| `NextBackupWindow` | [`NextBackupWindow`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/next-backup-window.md) | Required | The details of the Droplet's backups feature, if backups are configured for the Droplet. This object contains keys for the start and end times of the window during which the backup will start. | NextBackupWindow getNextBackupWindow() | setNextBackupWindow(NextBackupWindow nextBackupWindow) |
| `Region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/region.md) | Required | - | Region getRegion() | setRegion(Region region) |
| `Size` | [`Size`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/size.md) | Required | - | Size getSize() | setSize(Size size) |
| `SizeSlug` | `String` | Required | The unique slug identifier for the size of this Droplet. | String getSizeSlug() | setSizeSlug(String sizeSlug) |
| `SnapshotIds` | `List<Integer>` | Required | An array of snapshot IDs of any snapshots created from the Droplet instance. | List<Integer> getSnapshotIds() | setSnapshotIds(List<Integer> snapshotIds) |
| `Status` | [`Status8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-8.md) | Required | A status string indicating the state of the Droplet instance. This may be "new", "active", "off", or "archive". | Status8 getStatus() | setStatus(Status8 status) |
| `Tags` | `List<String>` | Required | An array of Tags the Droplet has been tagged with. | List<String> getTags() | setTags(List<String> tags) |
| `Vcpus` | `int` | Required | The number of virtual CPUs. | int getVcpus() | setVcpus(int vcpus) |
| `VolumeIds` | `List<String>` | Required | A flat array including the unique identifier for each Block Storage volume attached to the Droplet. | List<String> getVolumeIds() | setVolumeIds(List<String> volumeIds) |
| `VpcUuid` | `String` | Optional | A string specifying the UUID of the VPC to which the Droplet is assigned. | String getVpcUuid() | setVpcUuid(String vpcUuid) |
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
import com.digitalocean.api.models.Region2;
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

Droplet droplet = new Droplet.Builder(
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
.build();
```



