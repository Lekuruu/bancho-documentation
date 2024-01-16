# Message

| Size |  Datatype  | Description              |
|:----:|:----------:|:-------------------------|
|      | [[String]] | Sender (Name)            |
|      | [[String]] | Message                  |
|      | [[String]] | Target (Channel or User) |
|  4   |    sInt    | Sender (UserId)          |

In versions around b20121223 and lower, the sender is not present anymore:

| Size |  Datatype  | Description              |
|:----:|:----------:|:-------------------------|
|      | [[String]] | Sender (Name)            |
|      | [[String]] | Message                  |
|      | [[String]] | Target (Channel or User) |
