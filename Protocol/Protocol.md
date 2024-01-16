# Protocol

As explained in the previous document, the client will nowadays connect over **HTTPS**, under **c.ppy.sh**.
However, in 2008 until late 2013, the clients were connecting over TCP on port **13381**, with basically the same behaviour as today.

If a connection has been established, the client needs to login,
before it can interact with the server.
*See [[Login]]*

After that, the client will only send and receive bancho packets.

## Packet structure

A bancho packet is serialized with little-endian and is made up of a **header**, containing **packet id** and **packet size**, 
followed by the **packet content**, which depends on the packet id.

## Header

| Size | Datatype | Description  |
|:----:|:--------:|:------------:|
|  2   |  uShort  |  Packet ID   |
|  1   | boolean  | Compression  |
|  4   |   uInt   | Content Size |
|  ?   |          |   Content    |

If the compression boolean is true, the content is compressed with gzip.

## Legacy Header

In version b323 and below, the header looks a bit different:

| Size | Datatype | Description  |
|:----:|:--------:|:------------:|
|  2   |  uShort  |  Packet ID   |
|  4   |   uInt   | Content Size |
|  ?   |          |   Content    |

The gzip compression is enabled by default in these versions.

### Example

Here is an example for the [[LoginReply]] packet:

```
05 00 00 04 00 00 00 64 00 00 00
```

In this case, the *packet id* is **5** and the *packet size* is **4**.
The *content* contains an integer, which represents the user id of the player that is connecting to the server **100**.
