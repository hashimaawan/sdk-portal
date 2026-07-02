# Git

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkdpdA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Git`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `branch` | `str` | Optional | The name of the branch to use |
| `repo_clone_url` | `str` | Optional | The clone URL of the repo. Example: `https://github.com/digitalocean/sample-golang.git` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.git import Git

git = Git(
    branch='main',
    repo_clone_url='https://github.com/digitalocean/sample-golang.git',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



