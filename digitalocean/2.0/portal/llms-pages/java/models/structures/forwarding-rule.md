# Forwarding Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkZvcndhcmRpbmdSdWxl

An object specifying a forwarding rule for a load balancer.

*This model accepts additional fields of type Object.*


# Class Name

`ForwardingRule`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CertificateId` | `String` | Optional | The ID of the TLS certificate used for SSL termination if enabled. | String getCertificateId() | setCertificateId(String certificateId) |
| `EntryPort` | `int` | Required | An integer representing the port on which the load balancer instance will listen. | int getEntryPort() | setEntryPort(int entryPort) |
| `EntryProtocol` | [`EntryProtocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/entry-protocol.md) | Required | The protocol used for traffic to the load balancer. The possible values are: `http`, `https`, `http2`, `http3`, `tcp`, or `udp`. If you set the  `entry_protocol` to `udp`, the `target_protocol` must be set to `udp`.  When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. | EntryProtocol getEntryProtocol() | setEntryProtocol(EntryProtocol entryProtocol) |
| `TargetPort` | `int` | Required | An integer representing the port on the backend Droplets to which the load balancer will send traffic. | int getTargetPort() | setTargetPort(int targetPort) |
| `TargetProtocol` | [`TargetProtocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/target-protocol.md) | Required | The protocol used for traffic from the load balancer to the backend Droplets. The possible values are: `http`, `https`, `http2`, `tcp`, or `udp`. If you set the `target_protocol` to `udp`, the `entry_protocol` must be set to  `udp`. When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. | TargetProtocol getTargetProtocol() | setTargetProtocol(TargetProtocol targetProtocol) |
| `TlsPassthrough` | `Boolean` | Optional | A boolean value indicating whether SSL encrypted traffic will be passed through to the backend Droplets. | Boolean getTlsPassthrough() | setTlsPassthrough(Boolean tlsPassthrough) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.EntryProtocol;
import com.digitalocean.api.models.ForwardingRule;
import com.digitalocean.api.models.TargetProtocol;
import java.io.IOException;

ForwardingRule forwardingRule = new ForwardingRule.Builder(
    443,
    EntryProtocol.HTTPS,
    80,
    TargetProtocol.HTTP
)
.certificateId("892071a0-bb95-49bc-8021-3afd67a210bf")
.tlsPassthrough(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



