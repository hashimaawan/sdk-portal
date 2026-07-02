# Source

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlNvdXJjZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Source`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | `*string` | Optional, Read-only | The name of the default database. |
| `Host` | `*string` | Optional, Read-only | The FQDN pointing to the database cluster's current primary node. |
| `Password` | `*string` | Optional, Read-only | The randomly generated password for the default user. |
| `Port` | `*int` | Optional, Read-only | The port on which the database cluster is listening. |
| `Ssl` | `*bool` | Optional, Read-only | A boolean value indicating if the connection should be made over SSL. |
| `Uri` | `*string` | Optional, Read-only | A connection string in the format accepted by the `psql` command. This is provided as a convenience and should be able to be constructed by the other attributes. |
| `User` | `*string` | Optional, Read-only | The default user for the database. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    source := models.Source{
        Database:              models.ToPointer("defaultdb"),
        Host:                  models.ToPointer("backend-do-user-19081923-0.db.ondigitalocean.com"),
        Password:              models.ToPointer("wv78n3zpz42xezdk"),
        Port:                  models.ToPointer(25060),
        Ssl:                   models.ToPointer(true),
        Uri:                   models.ToPointer("postgres://doadmin:wv78n3zpz42xezdk@backend-do-user-19081923-0.db.ondigitalocean.com:25060/defaultdb?sslmode=require"),
        User:                  models.ToPointer("doadmin"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



