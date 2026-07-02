# Warning

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRldhcm5pbmc

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Warning`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Code` | [`Code?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/code.md) | Optional | A code identifier that represents the failing condition.<br><br>Failing conditions:<br><br>- `incompatible_phase` - indicates that the deployment's phase is not suitable for rollback.<br>- `incompatible_result` - indicates that the deployment's result is not suitable for rollback.<br>- `exceeded_revision_limit` - indicates that the app has exceeded the rollback revision limits for its tier.<br>- `app_pinned` - indicates that there is already a rollback in progress and the app is pinned.<br>- `database_config_conflict` - indicates that the deployment's database config is different than the current config.<br>- `region_conflict` - indicates that the deployment's region differs from the current app region.<br><br>Warning conditions:<br><br>- `static_site_requires_rebuild` - indicates that the deployment contains at least one static site that will require a rebuild.<br>- `image_source_missing_digest` - indicates that the deployment contains at least one component with an image source that is missing a digest. |
| `Components` | `List<string>` | Optional | - |
| `Message` | `string` | Optional | A human-readable message describing the failing condition. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Warning warning = new Warning
{
    Code = Code.ExceededRevisionLimit,
    Components = new List<string>
    {
        "www",
    },
    Message = "the deployment is past the maximum historical revision limit of 0 for the \"starter\" app tier",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



