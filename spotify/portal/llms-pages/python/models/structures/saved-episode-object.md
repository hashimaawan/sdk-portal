# Saved Episode Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRlNhdmVkRXBpc29kZU9iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`SavedEpisodeObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `added_at` | `datetime` | Optional | The date and time the episode was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ. |
| `episode` | [`EpisodeObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/episode-object.md) | Optional | Information about the episode. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.episode_object import EpisodeObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.episode_restriction_object import EpisodeRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.resume_point_object import ResumePointObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.saved_episode_object import SavedEpisodeObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.show_base import ShowBase

saved_episode_object = SavedEpisodeObject(
    added_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    episode=EpisodeObject(
        audio_preview_url='audio_preview_url8',
        description='description2',
        html_description='html_description8',
        duration_ms=46,
        explicit=False,
        external_urls=ExternalUrlObject(
            spotify='spotify6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        href='href4',
        id='id2',
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
        is_playable=False,
        languages=[
            'languages9',
            'languages0',
            'languages1'
        ],
        name='name2',
        release_date='release_date0',
        release_date_precision=ReleaseDatePrecision.YEAR,
        uri='uri6',
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
        language='language4',
        resume_point=ResumePointObject(
            fully_played=False,
            resume_position_ms=254,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        restrictions=EpisodeRestrictionObject(
            reason='reason0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



