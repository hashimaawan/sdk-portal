# Action 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFjdGlvbjE

The linked actions can be used to check the status of a Droplet's create event.

*This model accepts additional fields of type Object.*


# Class Name

`Action1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Href` | `String` | Optional | A URL that can be used to access the action. | String getHref() | setHref(String href) |
| `Id` | `Integer` | Optional | A unique numeric ID that can be used to identify and reference an action. | Integer getId() | setId(Integer id) |
| `Rel` | `String` | Optional | A string specifying the type of the related action. | String getRel() | setRel(String rel) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Action1;
import java.io.IOException;

Action1 action1 = new Action1.Builder()
    .href("https://api.digitalocean.com/v2/actions/7515")
    .id(7515)
    .rel("create")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



