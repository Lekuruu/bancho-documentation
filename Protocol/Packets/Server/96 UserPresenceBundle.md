# UserPresenceBundle

This was introduced sometime in 2012, which changed the way how user stats are being sent to the clients.

Instead of sending every user with their stats, you just send the user id to the client and let the client request the stats and presence of the user.

| Size |        Datatype        | Description |
|:----:|:----------------------:|:------------|
|      | [[UserPresenceBundle]] | Player IDs  |
