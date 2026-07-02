# Query Execution State 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGUx

<p>The state of query execution. <code>QUEUED</code> indicates that the query has been submitted to the service, and Athena will execute the query as soon as resources are available. <code>RUNNING</code> indicates that the query is in execution phase. <code>SUCCEEDED</code> indicates that the query completed without errors. <code>FAILED</code> indicates that the query experienced an error and did not complete processing. <code>CANCELLED</code> indicates that a user input interrupted query execution.</p> <note> <p>Athena automatically retries your queries in cases of certain transient errors. As a result, you may see the query state transition from <code>RUNNING</code> or <code>FAILED</code> to <code>QUEUED</code>. </p> </note>



# Class Name

`QueryExecutionState1Enum`


# Fields

| Name |
|  --- |
| `QUEUED` |
| `RUNNING` |
| `SUCCEEDED` |
| `FAILED` |
| `CANCELLED` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    queryExecutionState1 := models.QueryExecutionState1Enum_CANCELLED

}
```



