# Mode

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRk1vZGU

Indicates the modality (major or minor) of a section, the type of scale from which its melodic content is derived. This field will contain a 0 for "minor", a 1 for "major", or a -1 for no result. Note that the major key (e.g. C major) could more likely be confused with the minor key at 3 semitones lower (e.g. A minor) as both keys carry the same pitches.


# Enum Type Name

`Mode`


# Fields

| Name |
|  --- |
| `EnumMinus1` |
| `Enum0` |
| `Enum1` |


# Example

```ts
import {
  Mode,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const mode = Mode.EnumMinus1;
```



