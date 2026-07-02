# Status 10

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXR1czEw

An object containing a `state` attribute whose value is set to a string indicating the current status of the node.

*This model accepts additional fields of type Object.*


# Class Name

`Status10`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `State` | [`State1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/state-1.md) | Optional | A string indicating the current status of the node. | State1 getState() | setState(State1 state) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.State1;
import com.digitalocean.api.models.Status10;
import java.io.IOException;

Status10 status10 = new Status10.Builder()
    .state(State1.PROVISIONING)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



