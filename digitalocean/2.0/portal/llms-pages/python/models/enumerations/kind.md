# Kind

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRktpbmQ

- UNSPECIFIED: Default job type, will auto-complete to POST_DEPLOY kind.
- PRE_DEPLOY: Indicates a job that runs before an app deployment.
- POST_DEPLOY: Indicates a job that runs after an app deployment.
- FAILED_DEPLOY: Indicates a job that runs after a component fails to deploy.


# Enum Type Name

`Kind`


# Fields

| Name |
|  --- |
| `UNSPECIFIED` |
| `PRE_DEPLOY` |
| `POST_DEPLOY` |
| `FAILED_DEPLOY` |


# Example

```python
from digitaloceanapi.models.kind import Kind

kind = Kind.POST_DEPLOY
```



