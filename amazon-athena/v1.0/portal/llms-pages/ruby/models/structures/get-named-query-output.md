# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query` | [`NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/named-query-1.md) | Optional | - |


# Example

```ruby
get_named_query_output = GetNamedQueryOutput.new(
  NamedQuery1.new(
    'Name0',
    'Database8',
    'QueryString2',
    'Description6',
    'NamedQueryId2',
    'WorkGroup2'
  )
)
```



