# UserPresence

| Size |  Datatype  | Description              |
|:----:|:----------:|:-------------------------|
|  4   |    sInt    | UserId                   |
|      | [[String]] | Username                 |
|  1   |    char    | Timezone + 24            |
|  1   |    char    | CountryId                |
|  1   |    char    | Permissions \| Mode << 5 |
|  4   |   float    | Longitude                |
|  4   |   float    | Latitude                 |
|  4   |    sInt    | Rank                     |

::: info
The "CountryId", is the index of a country inside [this list](https://github.com/osuTitanic/common/blob/main/constants/country.py).
:::

::: info
The `Permissions | Mode << 5` operation packs the permissions and mode values into a single character by shifting the mode value 5 bits to the left and performing a bitwise OR with the permissions.
:::