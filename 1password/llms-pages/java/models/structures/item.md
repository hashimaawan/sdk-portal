# Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRkl0ZW0

*This model accepts additional fields of type Object.*


# Class Name

`Item`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Category` | [`Category`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/enumerations/category.md) | Required | - | Category getCategory() | setCategory(Category category) |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | - | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Favorite` | `Boolean` | Optional | **Default**: `false` | Boolean getFavorite() | setFavorite(Boolean favorite) |
| `Id` | `String` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` | String getId() | setId(String id) |
| `LastEditedBy` | `String` | Optional, Read-only | - | String getLastEditedBy() | setLastEditedBy(String lastEditedBy) |
| `State` | [`State`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/enumerations/state.md) | Optional, Read-only | - | State getState() | setState(State state) |
| `Tags` | `List<String>` | Optional | - | List<String> getTags() | setTags(List<String> tags) |
| `Title` | `String` | Optional | - | String getTitle() | setTitle(String title) |
| `UpdatedAt` | `LocalDateTime` | Optional, Read-only | - | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `Urls` | [`List<Url>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/url.md) | Optional | - | List<Url> getUrls() | setUrls(List<Url> urls) |
| `Vault` | [`Vault1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/vault-1.md) | Required | - | Vault1 getVault() | setVault(Vault1 vault) |
| `Version` | `Integer` | Optional | - | Integer getVersion() | setVersion(Integer version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import java.util.Arrays;
import local.m1password.ApiHelper;
import local.m1password.DateTimeHelper;
import local.m1password.models.Category;
import local.m1password.models.Item;
import local.m1password.models.State;
import local.m1password.models.Url;
import local.m1password.models.Vault1;

Item item = new Item.Builder(
    Category.SSH_KEY,
    new Vault1.Builder(
        "id6"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.favorite(false)
.id("id2")
.lastEditedBy("lastEditedBy8")
.state(State.ARCHIVED)
.urls(Arrays.asList(
        new Url.Builder(
            "https://example.com"
        )
        .primary(true)
        .build(),
        new Url.Builder(
            "https://example.org"
        )
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



