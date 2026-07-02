# A Step that Is Run as Part of the Deployment S Lifecycle

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkElMjUyMHN0ZXAlMjUyMHRoYXQlMjUyMGlzJTI1MjBydW4lMjUyMGFzJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhlJTI1MjBkZXBsb3ltZW50JTI1MjdzJTI1MjBsaWZlY3ljbGU

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`AStepThatIsRunAsPartOfTheDeploymentSLifecycle`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ComponentName` | `string` | Optional | - |
| `EndedAt` | `DateTime?` | Optional | - |
| `MessageBase` | `string` | Optional | The base of a human-readable description of the step intended to be combined with the component name for presentation. For example:<br><br>`message_base` = "Building service"<br>`component_name` = "api" |
| `Name` | `string` | Optional | - |
| `Reason` | [`Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/reason.md) | Optional | - |
| `StartedAt` | `DateTime?` | Optional | - |
| `Status` | [`Status2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status-2.md) | Optional | **Default**: `Status2.UNKNOWN` |
| `Steps` | [`object`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

AStepThatIsRunAsPartOfTheDeploymentSLifecycle aStepThatIsRunAsPartOfTheDeploymentSLifecycle = new AStepThatIsRunAsPartOfTheDeploymentSLifecycle
{
    ComponentName = "component",
    EndedAt = DateTime.ParseExact("2020-11-19T20:27:18Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    MessageBase = "Building service",
    Name = "example_step",
    Reason = new Reason
    {
        Code = "code2",
        Message = "message4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    StartedAt = DateTime.ParseExact("2020-11-19T20:27:18Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Status = Status2.Success,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



