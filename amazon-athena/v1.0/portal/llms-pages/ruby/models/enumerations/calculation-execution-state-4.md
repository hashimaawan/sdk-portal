# Calculation Execution State 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdGU0

<p> <code>CREATING</code> - The calculation is in the process of being created.</p> <p> <code>CREATED</code> - The calculation has been created and is ready to run.</p> <p> <code>QUEUED</code> - The calculation has been queued for processing.</p> <p> <code>RUNNING</code> - The calculation is running.</p> <p> <code>CANCELING</code> - A request to cancel the calculation has been received and the system is working to stop it.</p> <p> <code>CANCELED</code> - The calculation is no longer running as the result of a cancel request.</p> <p> <code>COMPLETED</code> - The calculation has completed without error.</p> <p> <code>FAILED</code> - The calculation failed and is no longer running.</p>



# Enum Type Name

`CalculationExecutionState4Enum`


# Fields

| Name |
|  --- |
| `CREATING` |
| `CREATED` |
| `QUEUED` |
| `RUNNING` |
| `CANCELING` |
| `CANCELED` |
| `COMPLETED` |
| `FAILED` |


# Example

```ruby
calculation_execution_state4 = CalculationExecutionState4Enum::CANCELING
```



