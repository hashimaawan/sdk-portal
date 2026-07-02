# Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk5ldHdvcmtz

The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is.

*This model accepts additional fields of type Object.*


# Class Name

`Networks`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `V4` | [`List<V4>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v4.md) | Optional | - | List<V4> getV4() | setV4(List<V4> v4) |
| `V6` | [`List<V6>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v6.md) | Optional | - | List<V6> getV6() | setV6(List<V6> v6) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Networks;
import com.digitalocean.api.models.Type10;
import com.digitalocean.api.models.Type11;
import com.digitalocean.api.models.V4;
import com.digitalocean.api.models.V6;
import java.io.IOException;
import java.util.Arrays;

Networks networks = new Networks.Builder()
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
    .build();
```



