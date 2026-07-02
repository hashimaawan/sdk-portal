# Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJ1bGU


# Enum Type Name

`Rule`


# Fields

| Name |
|  --- |
| `UnspecifiedRule` |
| `CpuUtilization` |
| `MemUtilization` |
| `RestartCount` |
| `DeploymentFailed` |
| `DeploymentLive` |
| `DomainFailed` |
| `DomainLive` |
| `FunctionsActivationCount` |
| `FunctionsAverageDurationMs` |
| `FunctionsErrorRatePerMinute` |
| `FunctionsAverageWaitTimeMs` |
| `FunctionsErrorCount` |
| `FunctionsGbRatePerSecond` |


# Example

```csharp
using DigitalOceanApi.Standard.Models;

Rule rule = Rule.FunctionsErrorRatePerMinute;
```



