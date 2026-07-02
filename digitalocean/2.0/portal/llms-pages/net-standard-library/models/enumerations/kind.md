# Kind

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRktpbmQ

- UNSPECIFIED: Default job type, will auto-complete to POST_DEPLOY kind.
- PRE_DEPLOY: Indicates a job that runs before an app deployment.
- POST_DEPLOY: Indicates a job that runs after an app deployment.
- FAILED_DEPLOY: Indicates a job that runs after a component fails to deploy.


# Enum Type Name

`Kind`


# Fields

| Name |
|  --- |
| `Unspecified` |
| `PreDeploy` |
| `PostDeploy` |
| `FailedDeploy` |


# Example

```csharp
using DigitalOceanApi.Standard.Models;

Kind kind = Kind.PostDeploy;
```



