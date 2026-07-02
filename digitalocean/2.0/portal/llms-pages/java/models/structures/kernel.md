# Kernel

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRktlcm5lbA

**Note**: All Droplets created after March 2017 use internal kernels by default.
These Droplets will have this attribute set to `null`.

The current [kernel](https://www.digitalocean.com/docs/droplets/how-to/kernel/)
for Droplets with externally managed kernels. This will initially be set to
the kernel of the base image when the Droplet is created.

*This model accepts additional fields of type Object.*


# Class Name

`Kernel`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `Integer` | Optional | A unique number used to identify and reference a specific kernel. | Integer getId() | setId(Integer id) |
| `Name` | `String` | Optional | The display name of the kernel. This is shown in the web UI and is generally a descriptive title for the kernel in question. | String getName() | setName(String name) |
| `Version` | `String` | Optional | A standard kernel version string representing the version, patch, and release information. | String getVersion() | setVersion(String version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Kernel;
import java.io.IOException;

Kernel kernel = new Kernel.Builder()
    .id(7515)
    .name("DigitalOcean GrubLoader v0.2 (20160714)")
    .version("2016.07.13-DigitalOcean_loader_Ubuntu")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



