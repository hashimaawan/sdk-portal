# Functions Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZ1bmN0aW9ucyUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`FunctionsComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Optional | - |
| `Namespace` | `string` | Optional | The namespace where the functions are deployed. |
| `SourceCommitHash` | `string` | Optional | The commit hash of the repository that was used to build this functions component. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

FunctionsComponentsThatArePartOfThisDeployment functionsComponentsThatArePartOfThisDeployment = new FunctionsComponentsThatArePartOfThisDeployment
{
    Name = "my-functions-component",
    MNamespace = "ap-b2a93513-8d9b-4223-9d61-5e7272c81c32",
    SourceCommitHash = "54d4a727f457231062439895000d45437c7bb405",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



