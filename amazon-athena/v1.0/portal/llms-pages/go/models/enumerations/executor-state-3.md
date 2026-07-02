# Executor State 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkV4ZWN1dG9yU3RhdGUz

<p>The processing state of the executor. A description of each state follows.</p> <p> <code>CREATING</code> - The executor is being started, including acquiring resources.</p> <p> <code>CREATED</code> - The executor has been started.</p> <p> <code>REGISTERED</code> - The executor has been registered.</p> <p> <code>TERMINATING</code> - The executor is in the process of shutting down.</p> <p> <code>TERMINATED</code> - The executor is no longer running.</p> <p> <code>FAILED</code> - Due to a failure, the executor is no longer running.</p>



# Class Name

`ExecutorState3`


# Fields

| Name |
|  --- |
| `Creating` |
| `Created` |
| `Registered` |
| `Terminating` |
| `Terminated` |
| `Failed` |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    executorState3 := models.ExecutorState3_Creating

}
```



