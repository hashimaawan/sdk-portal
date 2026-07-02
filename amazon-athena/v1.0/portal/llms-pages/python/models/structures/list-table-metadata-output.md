# List Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhT3V0cHV0


# Class Name

`ListTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `table_metadata_list` | [`List[TableMetadata]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/table-metadata.md) | Optional | - |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```python
import dateutil.parser

from amazonathena.models.column import Column
from amazonathena.models.list_table_metadata_output import ListTableMetadataOutput
from amazonathena.models.table_metadata import TableMetadata

list_table_metadata_output = ListTableMetadataOutput(
    table_metadata_list=[
        TableMetadata(
            name='Name2',
            create_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            last_access_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            table_type='TableType2',
            columns=[
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
                ),
                Column(
                    name='Name6',
                    mtype='Type6',
                    comment='Comment0'
                ),
                Column(
                    name='Name6',
                    mtype='Type6',
                    comment='Comment0'
                )
            ]
        ),
        TableMetadata(
            name='Name2',
            create_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            last_access_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            table_type='TableType2',
            columns=[
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
                ),
                Column(
                    name='Name6',
                    mtype='Type6',
                    comment='Comment0'
                ),
                Column(
                    name='Name6',
                    mtype='Type6',
                    comment='Comment0'
                )
            ]
        ),
        TableMetadata(
            name='Name2',
            create_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            last_access_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            table_type='TableType2',
            columns=[
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
                ),
                Column(
                    name='Name6',
                    mtype='Type6',
                    comment='Comment0'
                ),
                Column(
                    name='Name6',
                    mtype='Type6',
                    comment='Comment0'
                )
            ]
        )
    ],
    next_token='NextToken8'
)
```



