# Project

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByb2plY3Q

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Project`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was created. |
| `Description` | `string` | Optional | The description of the project. The maximum length is 255 characters.<br><br>**Constraints**: *Maximum Length*: `255` |
| `Environment` | [`Environment?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/environment.md) | Optional | The environment of the project's resources. |
| `Id` | `Guid?` | Optional, Read-only | The unique universal identifier of this project. |
| `Name` | `string` | Optional | The human-readable name for the project. The maximum length is 175 characters and the name must be unique.<br><br>**Constraints**: *Maximum Length*: `175` |
| `OwnerId` | `int?` | Optional, Read-only | The integer id of the project owner. |
| `OwnerUuid` | `string` | Optional, Read-only | The unique universal identifier of the project owner. |
| `Purpose` | `string` | Optional | The purpose of the project. The maximum length is 255 characters. It can<br>have one of the following values:<br><br>- Just trying out DigitalOcean<br>- Class project / Educational purposes<br>- Website or blog<br>- Web Application<br>- Service or API<br>- Mobile Application<br>- Machine learning / AI / Data processing<br>- IoT<br>- Operational / Developer tooling<br><br>If another value for purpose is specified, for example, "your custom purpose",<br>your purpose will be stored as `Other: your custom purpose`.<br><br>**Constraints**: *Maximum Length*: `255` |
| `UpdatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was updated. |
| `IsDefault` | `bool?` | Optional | If true, all resources will be added to this project if no project is specified. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

Project project = new Project
{
    CreatedAt = DateTime.ParseExact("2018-09-27T20:10:35Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Description = "My website API",
    Environment = Environment.Production,
    Id = new Guid("4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679"),
    Name = "my-web-api",
    OwnerId = 258992,
    OwnerUuid = "99525febec065ca37b2ffe4f852fd2b2581895e7",
    Purpose = "Service or API",
    UpdatedAt = DateTime.ParseExact("2018-09-27T20:10:35Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    IsDefault = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



