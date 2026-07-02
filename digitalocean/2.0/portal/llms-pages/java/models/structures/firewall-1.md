# Firewall 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkZpcmV3YWxsMQ

An object specifying allow and deny rules to control traffic to the load balancer.

*This model accepts additional fields of type Object.*


# Class Name

`Firewall1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Allow` | `List<String>` | Optional | the rules for allowing traffic to the load balancer (in the form 'ip:1.2.3.4' or 'cidr:1.2.0.0/16') | List<String> getAllow() | setAllow(List<String> allow) |
| `Deny` | `List<String>` | Optional | the rules for denying traffic to the load balancer (in the form 'ip:1.2.3.4' or 'cidr:1.2.0.0/16') | List<String> getDeny() | setDeny(List<String> deny) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Firewall1;
import java.io.IOException;
import java.util.Arrays;

Firewall1 firewall1 = new Firewall1.Builder()
    .allow(Arrays.asList(
        "ip:1.2.3.4",
        "cidr:2.3.0.0/16"
    ))
    .deny(Arrays.asList(
        "ip:1.2.3.4",
        "cidr:2.3.0.0/16"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



