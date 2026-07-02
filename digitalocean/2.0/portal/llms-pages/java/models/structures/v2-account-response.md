# V2 Account Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBY2NvdW50JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2AccountResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Account` | [`Account`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/account.md) | Optional | - | Account getAccount() | setAccount(Account account) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Account;
import com.digitalocean.api.models.Status;
import com.digitalocean.api.models.Team;
import com.digitalocean.api.models.V2AccountResponse;
import java.io.IOException;

V2AccountResponse v2AccountResponse = new V2AccountResponse.Builder()
    .account(new Account.Builder(
        248,
        "email6",
        false,
        164,
        Status.WARNING,
        "status_message8",
        "uuid6"
    )
    .team(new Team.Builder()
            .name("name0")
            .uuid("uuid6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



