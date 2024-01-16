# Login

When the client has established a connection to the server, it will send the following information separated by "\\r\\n":

|    Name     | Description                           |
|:-----------:|:--------------------------------------|
|  Username   | The username of the player            |
|  Password   | The md5 hash of the player's password |
| Client Info | See below                             |

The server will then respond with a LoginReply packet, containing either the player id or an error:

| Response | Description                                             |
|:--------:|:--------------------------------------------------------|
|    -6    | The player is using a test build and is not a supporter |
|    -5    | A server-side error occurred                            |
|    -4    | The account was not yet activated                       |
|    -3    | The account was banned                                  |
|    -2    | Update is needed                                        |
|    -1    | Username/Password incorrect                             |
| User ID  | Player has successfully logged in                       |

### After Login

The server will send some additional packets after the login was successful.
*See [[After Login]]*

## Client Info

The client info is separated by "|" and contains the following information:

|         Name          | Description                         |
|:---------------------:|:------------------------------------|
|      Build Name       | The client version (e.g. b20130303) |
|      UTC Offset       | The UTC offset of the PC            |
| Display City Location | Either 1 or 0 (True/False)          |
|      Client Hash      | See below                           |
|    Friendonly DMs     | Either 1 or 0 (True/False)          |

## Client Hash

The client hash is separated by ":" and contains the following information:

|          Name           | Description                                |
|:-----------------------:|:-------------------------------------------|
|  Executable Name Hash   | MD5 hash of the executable name (osu!.exe) |
|   Network Interfaces    | See below                                  |
| Network Interfaces Hash | MD5 hash of all physical addresses         |
|        Unique ID        | See below                                  |
|        Unique ID        | See below                                  |

### Network Interfaces

The network interface is a string of all [physical addresses](https://learn.microsoft.com/en-us/windows/win32/network-interfaces#network-interface-identifiers-and-properties) seperated by dots.
If a client is running under wine, then the string will just contain "runningunderwine".

### Unique IDs

Unique ids are used to identify new PC's and inform the player about them.

The **first one** is a md5 hashed **registry key** ("Software\\osu!\\UninstallID"), that is randomly generated when you first open the game.

The **second one** is a md5 hash of your disk drive signature.
