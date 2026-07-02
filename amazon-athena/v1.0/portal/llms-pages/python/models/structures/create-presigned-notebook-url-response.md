# Create Presigned Notebook Url Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVzcG9uc2U


# Class Name

`CreatePresignedNotebookUrlResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_url` | `str` | Required | - |
| `auth_token` | `str` | Required | **Constraints**: *Maximum Length*: `2048` |
| `auth_token_expiration_time` | `int` | Required | - |


# Example

```python
from amazonathena.models.create_presigned_notebook_url_response import CreatePresignedNotebookUrlResponse

create_presigned_notebook_url_response = CreatePresignedNotebookUrlResponse(
    notebook_url='NotebookUrl8',
    auth_token='AuthToken2',
    auth_token_expiration_time=54
)
```



