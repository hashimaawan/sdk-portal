# Destinations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRlc3RpbmF0aW9ucw

*This model accepts additional fields of type Object.*


# Class Name

`Destinations`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Addresses` | `List<String>` | Optional | An array of strings containing the IPv4 addresses, IPv6 addresses, IPv4 CIDRs, and/or IPv6 CIDRs to which the firewall will allow traffic. | List<String> getAddresses() | setAddresses(List<String> addresses) |
| `DropletIds` | `List<Integer>` | Optional | An array containing the IDs of the Droplets to which the firewall will allow traffic. | List<Integer> getDropletIds() | setDropletIds(List<Integer> dropletIds) |
| `KubernetesIds` | `List<String>` | Optional | An array containing the IDs of the Kubernetes clusters to which the firewall will allow traffic. | List<String> getKubernetesIds() | setKubernetesIds(List<String> kubernetesIds) |
| `LoadBalancerUids` | `List<String>` | Optional | An array containing the IDs of the load balancers to which the firewall will allow traffic. | List<String> getLoadBalancerUids() | setLoadBalancerUids(List<String> loadBalancerUids) |
| `Tags` | `List<String>` | Optional | - | List<String> getTags() | setTags(List<String> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Destinations;
import java.io.IOException;
import java.util.Arrays;

Destinations destinations = new Destinations.Builder()
    .addresses(Arrays.asList(
        "1.2.3.4",
        "18.0.0.0/8"
    ))
    .dropletIds(Arrays.asList(
        8043964
    ))
    .kubernetesIds(Arrays.asList(
        "41b74c5d-9bd0-5555-5555-a57c495b81a3"
    ))
    .loadBalancerUids(Arrays.asList(
        "4de7ac8b-495b-4884-9a69-1050c6793cd6"
    ))
    .tags(Arrays.asList(
        "tags7",
        "tags8",
        "tags9"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



