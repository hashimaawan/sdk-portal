# V2 Droplets Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing information about a resource to be scheduled for deletion.

*This model accepts additional fields of type Object.*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FloatingIps` | `List<String>` | Optional | An array of unique identifiers for the floating IPs to be scheduled for deletion. | List<String> getFloatingIps() | setFloatingIps(List<String> floatingIps) |
| `ReservedIps` | `List<String>` | Optional | An array of unique identifiers for the reserved IPs to be scheduled for deletion. | List<String> getReservedIps() | setReservedIps(List<String> reservedIps) |
| `Snapshots` | `List<String>` | Optional | An array of unique identifiers for the snapshots to be scheduled for deletion. | List<String> getSnapshots() | setSnapshots(List<String> snapshots) |
| `VolumeSnapshots` | `List<String>` | Optional | An array of unique identifiers for the volume snapshots to be scheduled for deletion. | List<String> getVolumeSnapshots() | setVolumeSnapshots(List<String> volumeSnapshots) |
| `Volumes` | `List<String>` | Optional | An array of unique identifiers for the volumes to be scheduled for deletion. | List<String> getVolumes() | setVolumes(List<String> volumes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2DropletsDestroyWithAssociatedResourcesSelectiveRequest;
import java.io.IOException;
import java.util.Arrays;

V2DropletsDestroyWithAssociatedResourcesSelectiveRequest v2DropletsDestroyWithAssociatedResourcesSelectiveRequest = new V2DropletsDestroyWithAssociatedResourcesSelectiveRequest.Builder()
    .floatingIps(Arrays.asList(
        "6186916"
    ))
    .reservedIps(Arrays.asList(
        "6186916"
    ))
    .snapshots(Arrays.asList(
        "61486916"
    ))
    .volumeSnapshots(Arrays.asList(
        "edb0478d-7436-11ea-86e6-0a58ac144b91"
    ))
    .volumes(Arrays.asList(
        "ba49449a-7435-11ea-b89e-0a58ac14480f"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



