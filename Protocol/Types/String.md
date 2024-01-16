# String

A string has three parts; a single byte which will be either 0x00, indicating that the next two parts are not present, or 0x0b, indicating that the next two parts are present. 

If it is 0x0b, there will then be a **ULEB128**, representing the byte length of the following string, and then the string itself, encoded in UTF-8.

(https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)

**Example**:

"Hello, World!"

```
\x0b\rHello, World!
```