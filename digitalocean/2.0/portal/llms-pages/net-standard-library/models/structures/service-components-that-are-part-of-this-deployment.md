# Service Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZpY2UlMjUyMGNvbXBvbmVudHMlMjUyMHRoYXQlMjUyMGFyZSUyNTIwcGFydCUyNTIwb2YlMjUyMHRoaXMlMjUyMGRlcGxveW1lbnQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`ServiceComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Optional | - |
| `SourceCommitHash` | `string` | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

ServiceComponentsThatArePartOfThisDeployment serviceComponentsThatArePartOfThisDeployment = new ServiceComponentsThatArePartOfThisDeployment
{
    Name = "web",
    SourceCommitHash = "54d4a727f457231062439895000d45437c7bb405",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



