# BeatmapInfo

This type contains information about a beatmap, and the user's personal records on the map.

| Size |   Datatype   | Description  |
|:----:|:------------:|:-------------|
|  2   |    sShort    | Id           |
|  4   |     sInt     | BeatmapId    |
|  4   |     sInt     | BeatmapSetId |
|  4   |     sInt     | ThreadId     |
|  1   |     char     | Ranked       |
|  1   | [[Rankings]] | OsuRank      |
|  1   | [[Rankings]] | FruitsRank   |
|  1   | [[Rankings]] | TaikoRank    |
|  1   | [[Rankings]] | ManiaRank    |
|      |  [[String]]  | Beatmap MD5  |

::: info
The "Ranked" value contains the submission status:

- 1: Ranked
- 2: Approved
- 3: Pending
:::

::: info
The "Id" is the index of the requested filename, or `-1` if it was a requested BeatmapId.
:::

In versions **b20121008** and lower, the ManiaRank is not present anymore:

| Size |   Datatype   | Description  |
|:----:|:------------:|:-------------|
|  2   |    sShort    | Id           |
|  4   |     sInt     | BeatmapId    |
|  4   |     sInt     | BeatmapSetId |
|  4   |     sInt     | ThreadId     |
|  1   |     char     | Ranked       |
|  1   | [[Rankings]] | OsuRank      |
|  1   | [[Rankings]] | FruitsRank   |
|  1   | [[Rankings]] | TaikoRank    |
|      |  [[String]]  | Beatmap MD5  |