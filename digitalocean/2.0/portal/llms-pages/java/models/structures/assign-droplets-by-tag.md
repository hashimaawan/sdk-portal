# Assign Droplets by Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFzc2lnbiUyNTIwRHJvcGxldHMlMjUyMGJ5JTI1MjBUYWc

*This model accepts additional fields of type Object.*


# Class Name

`AssignDropletsByTag`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Tag` | `String` | Required | The name of a Droplet tag corresponding to Droplets assigned to the load balancer. | String getTag() | setTag(String tag) |
| `Region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. | Region2 getRegion() | setRegion(Region2 region) |
| `Algorithm` | [`Algorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/algorithm.md) | Optional | This field has been deprecated. You can no longer specify an algorithm for load balancers.<br><br>**Default**: `Algorithm.ROUND_ROBIN` | Algorithm getAlgorithm() | setAlgorithm(Algorithm algorithm) |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the load balancer was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `DisableLetsEncryptDnsRecords` | `Boolean` | Optional | A boolean value indicating whether to disable automatic DNS record creation for Let's Encrypt certificates that are added to the load balancer.<br><br>**Default**: `false` | Boolean getDisableLetsEncryptDnsRecords() | setDisableLetsEncryptDnsRecords(Boolean disableLetsEncryptDnsRecords) |
| `EnableBackendKeepalive` | `Boolean` | Optional | A boolean value indicating whether HTTP keepalive connections are maintained to target Droplets.<br><br>**Default**: `false` | Boolean getEnableBackendKeepalive() | setEnableBackendKeepalive(Boolean enableBackendKeepalive) |
| `EnableProxyProtocol` | `Boolean` | Optional | A boolean value indicating whether PROXY Protocol is in use.<br><br>**Default**: `false` | Boolean getEnableProxyProtocol() | setEnableProxyProtocol(Boolean enableProxyProtocol) |
| `Firewall` | [`Firewall1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/firewall-1.md) | Optional | An object specifying allow and deny rules to control traffic to the load balancer. | Firewall1 getFirewall() | setFirewall(Firewall1 firewall) |
| `ForwardingRules` | [`List<ForwardingRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/forwarding-rule.md) | Required | An array of objects specifying the forwarding rules for a load balancer.<br><br>**Constraints**: *Minimum Items*: `1` | List<ForwardingRule> getForwardingRules() | setForwardingRules(List<ForwardingRule> forwardingRules) |
| `HealthCheck` | [`HealthCheck1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/health-check-1.md) | Optional | An object specifying health check settings for the load balancer. | HealthCheck1 getHealthCheck() | setHealthCheck(HealthCheck1 healthCheck) |
| `HttpIdleTimeoutSeconds` | `Integer` | Optional | An integer value which configures the idle timeout for HTTP requests to the target droplets.<br><br>**Default**: `60`<br><br>**Constraints**: `>= 30`, `<= 600` | Integer getHttpIdleTimeoutSeconds() | setHttpIdleTimeoutSeconds(Integer httpIdleTimeoutSeconds) |
| `Id` | `UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a load balancer. | UUID getId() | setId(UUID id) |
| `Ip` | `String` | Optional, Read-only | An attribute containing the public-facing IP address of the load balancer.<br><br>**Constraints**: *Pattern*: `^$\|^((25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)\.){3}(25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)$` | String getIp() | setIp(String ip) |
| `Name` | `String` | Optional | A human-readable name for a load balancer instance. | String getName() | setName(String name) |
| `ProjectId` | `String` | Optional | The ID of the project that the load balancer is associated with. If no ID is provided at creation, the load balancer associates with the user's default project. If an invalid project ID is provided, the load balancer will not be created. | String getProjectId() | setProjectId(String projectId) |
| `RedirectHttpToHttps` | `Boolean` | Optional | A boolean value indicating whether HTTP requests to the load balancer on port 80 will be redirected to HTTPS on port 443.<br><br>**Default**: `false` | Boolean getRedirectHttpToHttps() | setRedirectHttpToHttps(Boolean redirectHttpToHttps) |
| `Size` | [`Size2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/size-2.md) | Optional | This field has been replaced by the `size_unit` field for all regions except in AMS2, NYC2, and SFO1. Each available load balancer size now equates to the load balancer having a set number of nodes.<br><br>* `lb-small` = 1 node<br>* `lb-medium` = 3 nodes<br>* `lb-large` = 6 nodes<br><br>You can resize load balancers after creation up to once per hour. You cannot resize a load balancer within the first hour of its creation.<br><br>**Default**: `Size2.LBSMALL` | Size2 getSize() | setSize(Size2 size) |
| `SizeUnit` | `Integer` | Optional | How many nodes the load balancer contains. Each additional node increases the load balancer's ability to manage more connections. Load balancers can be scaled up or down, and you can change the number of nodes after creation up to once per hour. This field is currently not available in the AMS2, NYC2, or SFO1 regions. Use the `size` field to scale load balancers that reside in these regions.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1`, `<= 100` | Integer getSizeUnit() | setSizeUnit(Integer sizeUnit) |
| `Status` | [`Status12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-12.md) | Optional, Read-only | A status string indicating the current state of the load balancer. This can be `new`, `active`, or `errored`. | Status12 getStatus() | setStatus(Status12 status) |
| `StickySessions` | [`StickySessions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/sticky-sessions.md) | Optional | An object specifying sticky sessions settings for the load balancer. | StickySessions getStickySessions() | setStickySessions(StickySessions stickySessions) |
| `VpcUuid` | `UUID` | Optional | A string specifying the UUID of the VPC to which the load balancer is assigned. | UUID getVpcUuid() | setVpcUuid(UUID vpcUuid) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Algorithm;
import com.digitalocean.api.models.AssignDropletsByTag;
import com.digitalocean.api.models.EntryProtocol;
import com.digitalocean.api.models.ForwardingRule;
import com.digitalocean.api.models.Region2;
import com.digitalocean.api.models.Size2;
import com.digitalocean.api.models.Status12;
import com.digitalocean.api.models.TargetProtocol;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

AssignDropletsByTag assignDropletsByTag = new AssignDropletsByTag.Builder(
    "prod:web",
    Region2.NYC3,
    Arrays.asList(
        new ForwardingRule.Builder(
            443,
            EntryProtocol.HTTPS,
            80,
            TargetProtocol.HTTP
        )
        .certificateId("892071a0-bb95-49bc-8021-3afd67a210bf")
        .tlsPassthrough(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.algorithm(Algorithm.ROUND_ROBIN)
.createdAt(DateTimeHelper.fromRfc8601DateTime("2017-02-01T22:22:58Z"))
.disableLetsEncryptDnsRecords(true)
.enableBackendKeepalive(true)
.enableProxyProtocol(true)
.httpIdleTimeoutSeconds(90)
.id(UUID.fromString("4de7ac8b-495b-4884-9a69-1050c6793cd6"))
.ip("104.131.186.241")
.name("example-lb-01")
.projectId("4de7ac8b-495b-4884-9a69-1050c6793cd6")
.redirectHttpToHttps(true)
.size(Size2.LBSMALL)
.sizeUnit(3)
.status(Status12.ENUM_NEW)
.vpcUuid(UUID.fromString("c33931f2-a26a-4e61-b85c-4e95a2ec431b"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



