# BeatmapInfoRequest

A packet to request beatmap information and personal records.
The server will respond with the [[BeatmapInfoReply]] packet afterwards.

| Size |    Datatype    | Description         |
|:----:|:--------------:|:--------------------|
|  4   |      sInt      | Amount of Filenames |
|      | List[[String]] | Filenames           |
|  4   |      sInt      | Amount of Ids       |
|      |   List[sInt]   | Beatmap Ids         |

This changed in ~b483, where only the filenames are requested:

| Size |    Datatype    | Description         |
|:----:|:--------------:|:--------------------|
|  4   |      sInt      | Amount of Filenames |
|      | List[[String]] | Filenames           |