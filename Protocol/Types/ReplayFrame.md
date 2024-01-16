# ReplayFrame

| Size |    Datatype     | Description           |
|:----:|:---------------:|:----------------------|
|  1   | [[ButtonState]] | What keys are pressed |
|  1   |      char       | See explanation below |
|  4   |      float      | MouseX                |
|  4   |      float      | MouseY                |
|  4   |      sInt       | Time                  |

The format is a bit different in b338, where the ButtonState was not present:

| Size | Datatype | Description |
|:----:|:--------:|:------------|
|  1   |   char   | RightClick  |
|  1   |   char   | LeftClick   |
|  4   |  float   | MouseX      |
|  4   |  float   | MouseY      |
|  4   |   sInt   | Time        |

This is also why the "char" after the ButtonState was still kept, since it would otherwise break the replays.
