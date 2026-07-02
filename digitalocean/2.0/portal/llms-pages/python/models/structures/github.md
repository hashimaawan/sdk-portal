# Github

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkdpdGh1Yg

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Github`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `branch` | `str` | Optional | The name of the branch to use |
| `deploy_on_push` | `bool` | Optional | Whether to automatically deploy new commits made to the repo |
| `repo` | `str` | Optional | The name of the repo in the format owner/repo. Example: `digitalocean/sample-golang` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.github import Github

github = Github(
    branch='main',
    deploy_on_push=True,
    repo='digitalocean/sample-golang',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



