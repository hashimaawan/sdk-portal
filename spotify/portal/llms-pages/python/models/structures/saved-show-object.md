# Saved Show Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRlNhdmVkU2hvd09iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`SavedShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `added_at` | `datetime` | Optional | The date and time the show was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `show` | [`ShowBase`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/show-base.md) | Optional | Information about the show. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.saved_show_object import SavedShowObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.show_base import ShowBase

saved_show_object = SavedShowObject(
    added_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    show=ShowBase(
        available_markets=[
            'available_markets0',
            'available_markets1',
            'available_markets2'
        ],
        copyrights=[
            CopyrightObject(
                text='text2',
                mtype='type2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            CopyrightObject(
                text='text2',
                mtype='type2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            CopyrightObject(
                text='text2',
                mtype='type2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        description='description4',
        html_description='html_description4',
        explicit=False,
        external_urls=ExternalUrlObject(
            spotify='spotify6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        href='href8',
        id='id6',
        images=[
            ImageObject(
                url='url6',
                height=182,
                width=222,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            ImageObject(
                url='url6',
                height=182,
                width=222,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            ImageObject(
                url='url6',
                height=182,
                width=222,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        is_externally_hosted=False,
        languages=[
            'languages7',
            'languages6',
            'languages5'
        ],
        media_type='media_type6',
        name='name6',
        publisher='publisher6',
        uri='uri0',
        total_episodes=198,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



