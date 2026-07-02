# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data_catalogs_summary` | [`Array[DataCatalogSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/data-catalog-summary.md) | Optional | - |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ruby
list_data_catalogs_output = ListDataCatalogsOutput.new(
  [
    DataCatalogSummary.new(
      'CatalogName4',
      DataCatalogType2Enum::HIVE
    ),
    DataCatalogSummary.new(
      'CatalogName4',
      DataCatalogType2Enum::HIVE
    ),
    DataCatalogSummary.new(
      'CatalogName4',
      DataCatalogType2Enum::HIVE
    )
  ],
  'NextToken2'
)
```



