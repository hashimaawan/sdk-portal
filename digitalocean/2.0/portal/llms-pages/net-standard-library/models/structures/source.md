# Source

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNvdXJjZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Source`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | `string` | Optional, Read-only | The name of the default database. |
| `Host` | `string` | Optional, Read-only | The FQDN pointing to the database cluster's current primary node. |
| `Password` | `string` | Optional, Read-only | The randomly generated password for the default user. |
| `Port` | `int?` | Optional, Read-only | The port on which the database cluster is listening. |
| `Ssl` | `bool?` | Optional, Read-only | A boolean value indicating if the connection should be made over SSL. |
| `Uri` | `string` | Optional, Read-only | A connection string in the format accepted by the `psql` command. This is provided as a convenience and should be able to be constructed by the other attributes. |
| `User` | `string` | Optional, Read-only | The default user for the database. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Source source = new Source
{
    Database = "defaultdb",
    Host = "backend-do-user-19081923-0.db.ondigitalocean.com",
    Password = "wv78n3zpz42xezdk",
    Port = 25060,
    Ssl = true,
    Uri = "postgres://doadmin:wv78n3zpz42xezdk@backend-do-user-19081923-0.db.ondigitalocean.com:25060/defaultdb?sslmode=require",
    User = "doadmin",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



