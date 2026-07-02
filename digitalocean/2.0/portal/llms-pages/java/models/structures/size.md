# Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlNpemU

*This model accepts additional fields of type Object.*


# Class Name

`Size`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Available` | `boolean` | Required | This is a boolean value that represents whether new Droplets can be created with this size.<br><br>**Default**: `true` | boolean getAvailable() | setAvailable(boolean available) |
| `Description` | `String` | Required | A string describing the class of Droplets created from this size. For example: Basic, General Purpose, CPU-Optimized, Memory-Optimized, or Storage-Optimized. | String getDescription() | setDescription(String description) |
| `Disk` | `int` | Required | The amount of disk space set aside for Droplets of this size. The value is represented in gigabytes. | int getDisk() | setDisk(int disk) |
| `Memory` | `int` | Required | The amount of RAM allocated to Droplets created of this size. The value is represented in megabytes.<br><br>**Constraints**: `>= 8`, *Multiple Of*: `8` | int getMemory() | setMemory(int memory) |
| `PriceHourly` | `double` | Required | This describes the price of the Droplet size as measured hourly. The value is measured in US dollars. | double getPriceHourly() | setPriceHourly(double priceHourly) |
| `PriceMonthly` | `double` | Required | This attribute describes the monthly cost of this Droplet size if the Droplet is kept for an entire month. The value is measured in US dollars. | double getPriceMonthly() | setPriceMonthly(double priceMonthly) |
| `Regions` | `List<String>` | Required | An array containing the region slugs where this size is available for Droplet creates. | List<String> getRegions() | setRegions(List<String> regions) |
| `Slug` | `String` | Required | A human-readable string that is used to uniquely identify each size. | String getSlug() | setSlug(String slug) |
| `Transfer` | `double` | Required | The amount of transfer bandwidth that is available for Droplets created in this size. This only counts traffic on the public interface. The value is given in terabytes. | double getTransfer() | setTransfer(double transfer) |
| `Vcpus` | `int` | Required | The integer of number CPUs allocated to Droplets of this size. | int getVcpus() | setVcpus(int vcpus) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Size;
import java.io.IOException;
import java.util.Arrays;

Size size = new Size.Builder(
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
.build();
```



