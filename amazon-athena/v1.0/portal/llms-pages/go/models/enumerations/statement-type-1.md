# Statement Type 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXRlbWVudFR5cGUx

The type of query statement that was run. <code>DDL</code> indicates DDL query statements. <code>DML</code> indicates DML (Data Manipulation Language) query statements, such as <code>CREATE TABLE AS SELECT</code>. <code>UTILITY</code> indicates query statements other than DDL and DML, such as <code>SHOW CREATE TABLE</code>, or <code>DESCRIBE TABLE</code>.


# Class Name

`StatementType1`


# Fields

| Name |
|  --- |
| `Ddl` |
| `Dml` |
| `Utility` |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    statementType1 := models.StatementType1_Ddl

}
```



