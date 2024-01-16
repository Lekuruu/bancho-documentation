# Match

The bMatch type has changed a lot over the years. The current format looks like this:

| Size |  Datatype  | Description                                  |
|:----:|:----------:|:---------------------------------------------|
|  2   |   sShort   | Match ID                                     |
|  1   |    bool    | In Progress                                  |
|  1   |    char    | Match Type                                   |
|  4   |    sInt    | Mods                                         |
|      | [[String]] | Name                                         |
|      | [[String]] | Password                                     |
|      | [[String]] | Beatmap Text                                 |
|  4   |    sInt    | Beatmap ID                                   |
|      | [[String]] | Beatmap Checksum                             |
|  16  | char * 16  | Slot Status for each Slot                    |
|  16  | char * 16  | Slot Team for each Slot                      |
|  64  | sInt * 16  | Player ID for each Slot                      |
|  4   |    sInt    | Player ID of Host                            |
|  1   |    char    | Mode                                         |
|  1   |    char    | Scoring Type                                 |
|  1   |    char    | Team Type                                    |
|  1   |    bool    | Freemod                                      |
|  64  | sInt * 16  | Mods for each Slot (only if freemod is true) |
|  4   |    sInt    | Match Seed for the osu!mania "Random" mod    |