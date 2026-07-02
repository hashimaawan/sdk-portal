# Get Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFPdXRwdXQ


# Class Name

`GetTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `table_metadata` | [`TableMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/table-metadata-2.md) | Optional | - |


# Example

```python
import dateutil.parser

from amazonathena.models.column import Column
from amazonathena.models.get_table_metadata_output import GetTableMetadataOutput
from amazonathena.models.table_metadata_2 import TableMetadata2

get_table_metadata_output = GetTableMetadataOutput(
    table_metadata=TableMetadata2(
        name='Name6',
        create_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        last_access_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        table_type='TableType0',
        columns=[
            Column(
                name='Name0',
                mtype='Type0',
                comment='Comment4'
            ),
            Column(
                name='Name0',
                mtype='Type0',
                comment='Comment4'
            ),
            Column(
                name='Name0',
                mtype='Type0',
                comment='Comment4'
            )
        ],
        partition_keys=[
            Column(
                name='Name6',
                mtype='Type6',
                comment='Comment0'
            )
        ]
    )
)
```



