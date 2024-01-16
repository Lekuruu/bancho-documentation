# ReplayFrameBundle

| Size |         Datatype         | Description           |
|:----:|:------------------------:|:----------------------|
|  4   |           sInt           | "Extra"               |
|  2   |          uShort          | Bundle Length         |
|      |  List[[[ReplayFrame]]]   | List of Replay Frames |
|  1   |     [[ReplayAction]]     | Replay Action         |
|      | Optional[[[ScoreFrame]]] | ScoreFrame (Optional) |

::: info
"Extra" is used for either the user id that the user is spectating,
or the seed the user has for the osu!mania Random mod.
:::
