# Links

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxpbmtz

*This model accepts additional fields of type Object.*


# Class Name

`Links`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Pages` | [`LinksPages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/links-pages.md) | Optional | This is a container for any-of cases. | LinksPages getPages() | setPages(LinksPages pages) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;

Links links = new Links.Builder()
    .pages(LinksPages.fromPages(
        new Pages.Builder()
            .last("last6")
            .next("next2")
        .additionalProperty("pages", ApiHelper.deserialize("{\"first\":\"https://api.digitalocean.com/v2/account/keys?page=1\",\"prev\":\"https://api.digitalocean.com/v2/account/keys?page=2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



