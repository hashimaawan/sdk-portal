# Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJ1bGU


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

```ts
import { Rule } from 'digitalocean-apilib';

const rule = Rule.FunctionsErrorRatePerMinute;
```



