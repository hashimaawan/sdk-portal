# Section Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlNlY3Rpb25PYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`SectionObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `start` | `Float` | Optional | The starting point (in seconds) of the section. |
| `duration` | `Float` | Optional | The duration (in seconds) of the section. |
| `confidence` | `Float` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the section's "designation".<br><br>**Constraints**: `>= 0`, `<= 1` |
| `loudness` | `Float` | Optional | The overall loudness of the section in decibels (dB). Loudness values are useful for comparing relative loudness of sections within tracks. |
| `tempo` | `Float` | Optional | The overall estimated tempo of the section in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration. |
| `tempo_confidence` | `Float` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the tempo. Some tracks contain tempo changes or sounds which don't contain tempo (like pure speech) which would correspond to a low value in this field.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `key` | `Integer` | Optional | The estimated overall key of the section. The values in this field ranging from 0 to 11 mapping to pitches using standard Pitch Class notation (E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on). If no key was detected, the value is -1. |
| `key_confidence` | `Float` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the key. Songs with many key changes may correspond to low values in this field.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `mode` | [`Mode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/enumerations/mode.md) | Optional | Indicates the modality (major or minor) of a section, the type of scale from which its melodic content is derived. This field will contain a 0 for "minor", a 1 for "major", or a -1 for no result. Note that the major key (e.g. C major) could more likely be confused with the minor key at 3 semitones lower (e.g. A minor) as both keys carry the same pitches. |
| `mode_confidence` | `Float` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the `mode`.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `time_signature` | `Integer` | Optional | An estimated time signature. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure). The time signature ranges from 3 to 7 indicating time signatures of "3/4", to "7/4".<br><br>**Constraints**: `>= 3`, `<= 7` |
| `time_signature_confidence` | `Float` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the `time_signature`. Sections with time signature changes may correspond to low values in this field.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
section_object = SectionObject.new(
  start: 0,
  duration: 6.97092,
  confidence: 1,
  loudness: -14.938,
  tempo: 113.178,
  tempo_confidence: 0.647,
  key: 9,
  key_confidence: 0.297,
  mode_confidence: 0.471,
  time_signature: 4,
  time_signature_confidence: 1,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



