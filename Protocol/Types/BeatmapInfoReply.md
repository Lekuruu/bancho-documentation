# BeatmapInfoReply

This will get sent as a result of the [[BeatmapInfoRequest]] packet.

| Size |      Datatype       | Description        |
|:----:|:-------------------:|:-------------------|
|  4   |        sInt         | Amount of Beatmaps |
|      | List[[BeatmapInfo]] | BeatmapInfos       |