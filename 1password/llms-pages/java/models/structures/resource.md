# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRlJlc291cmNl

*This model accepts additional fields of type Object.*


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Item` | [`Item2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/item-2.md) | Optional | - | Item2 getItem() | setItem(Item2 item) |
| `ItemVersion` | `Integer` | Optional | - | Integer getItemVersion() | setItemVersion(Integer itemVersion) |
| `Type` | [`Type`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/enumerations/type.md) | Optional | - | Type getType() | setType(Type type) |
| `Vault` | [`Vault3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/vault-3.md) | Optional | - | Vault3 getVault() | setVault(Vault3 vault) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import local.m1password.ApiHelper;
import local.m1password.models.Item2;
import local.m1password.models.Resource;
import local.m1password.models.Type;
import local.m1password.models.Vault3;

Resource resource = new Resource.Builder()
    .item(new Item2.Builder()
        .id("id2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .itemVersion(108)
    .type(Type.ITEM)
    .vault(new Vault3.Builder()
        .id("id6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



