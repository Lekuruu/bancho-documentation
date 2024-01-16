# After Login

The server will send some packets after the login was successful.

**NOTE:**
In order to perform a full login, the client needs to join #osu.
The client will only display the "Welcome to Bancho!" text if this is done.
Else it will just be stuck at the "Receiving Data" text.

### Login Reply

This will contain the id of the user that is logging in. If the login failed, it contains an error
code, that the client can use to give the player more information.

Reference: [[5 LoginReply]]

### Permissions

This will send the current permissions for the player, which tells the client if they have access to
osu!direct, if they are a BAT, and more.

Reference: [[71 LoginPermissions]]

### Player Presence & Stats

This contains information about the player that is logging in. In the early versions of bancho, this
was accessible in a single packet, but was later split up to two packets, to improve performance.

Reference: [[Players]] ([[11 UserStats]], [[83 UserPresence]])

### Friends

A list of user ids, containing the players friends.

Reference: [[72 FriendsList]]

### Channels

A list of channels, including their name, description and user count.
When all channels have been sent, the client will get a "ChannelListComplete" packet.

Reference: [[Channels]] ([[65 ChannelAvailable]], [[67 ChannelAvailableAutojoin]], [[89 ChannelInfoComplete]])

### Online Players

A list of all currently online players. In earlier versions of bancho, this would contain the full stats
for each player, but was changed to just be a list of user ids, to improve performance.

Reference: [[Players]] ([[11 UserStats]], [[83 UserPresence]], [[95 UserPresenceSingle]], [[96 UserPresenceBundle]])

### Menu Icon (optional)

A packet that was introduced in bXXX, which contains a link to an image, which will be displayed
inside the menu. Additionally, there is a link that the player will be redirected to when they click
on the image.

Reference: [[76 MenuIcon]]

### Silence Info (optional)

This would contain the amount of time the player is silenced, if the player is silenced. This would prevent
the player from sending messages, and would also make them unable to switch accounts, until they are unsilenced.

Reference: [[92 SilenceInfo]]