# voice

## Description

Fired every time that voice data has been received.

## Example

Credits to [FlowerHvH1337](https://gamesense.pub/forums/profile.php?id=6321) for this example:

```lua
local voice_data_t = ffi.typeof[[    struct {        char     pad_0000[8];        int32_t  client;        int32_t  audible_mask;        uint64_t xuid;        void*    voice_data;        bool     proximity;        bool     caster;        char     pad_001E[2];        int32_t  format;        int32_t  sequence_bytes;        uint32_t section_number;        uint32_t uncompressed_sample_offset;        char     pad_0030[4];        uint32_t has_bits;    } *]]client.set_event_callback("voice", function(e)    local data = e.data    local voice_data = ffi.cast(voice_data_t, data)end)
```
