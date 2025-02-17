# Native MIDI

## Options

| Name              | Default | Min | Max  | Description |
|-------------------|---------|-----|------|-------------|
| midi_complevel    |       1 |   0 |    2 | Compatibility level. <br><li> 0 - (Vanilla) emulates Doom's DMX driver. <br><li> 1 - (Standard) emulates Microsoft GS Wavetable Synth. <br><li> 2 - (Full) sends all MIDI messages. |
| midi_reset_type   |       1 |   0 |    3 | Reset type. <br> "No SysEx" is a partial reset for devices that don't support SysEx messages. <br><li> 0 - No SysEx <br><li> 1 - GM <br><li> 2 - GS <br><li> 3 - XG <br> |
| midi_reset_delay  |      -1 |  -1 | 2000 | Delay after reset. <br> Hardware devices require time to execute a reset. If the first few notes of a song are cut off, try increasing this value. <br><li> -1 - Auto <br><li> 0 - None <br><li> 1-2000 - Milliseconds. |
| midi_ctf          |       1 |   0 |    1 | Fix invalid instruments by emulating SC-55 capital tone fallback (CTF). <br> This may help with missing notes, pianos sounds, or silence caused by incorrectly written songs.
| midi_sysex_volume |       0 |   0 |    1 | Use SysEx messages to control volume. <br> Useful for real or emulated hardware MIDI devices when making adjustments to the above options. |
| midi_gain         |       0 | -20 |    0 | Gain [dB] adjustment for native MIDI only. <br> Does not affect other music types. |

## Channel and System Messages

| Status Byte | Vanilla            | Standard           | Full               | MIDI Message |
|-------------|--------------------|--------------------|--------------------|--------------|
| 0x8n        | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Note Off |
| 0x9n        | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Note On |
| 0xAn        | :x:                | :x:                | :heavy_check_mark: | Polyphonic Key Pressure (Aftertouch) |
| 0xBn        | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Control Change (Controller) |
| 0xCn        | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Program Change |
| 0xDn        | :x:                | :x:                | :heavy_check_mark: | Channel Pressure (Channel Aftertouch) |
| 0xEn        | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Pitch Bend |
| 0xF0        | :x:                | :x:                | :heavy_check_mark: | SysEx SOX |
| 0xF7        | :x:                | :x:                | :heavy_check_mark: | SysEx EOX |
| 0xFF        | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Meta Message |

## Meta Messages
| Meta Type | Vanilla            | Standard           | Full               | Function |
|-----------|--------------------|--------------------|--------------------|----------|
| 0x06      | :x:                | :heavy_check_mark: | :heavy_check_mark: | Marker (Final Fantasy: loopStart, loopEnd) |
| 0x2F      | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | End of Track |
| 0x51      | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Set Tempo |

## Registered Parameter Numbers

| RPN MSB | RPN LSB | Vanilla | Standard           | Full               | Function |
|---------|---------|---------|--------------------|--------------------|----------|
| 0x00    | 0x00    | :x:     | :heavy_check_mark: | :heavy_check_mark: | Pitch Bend Sensitivity |
| 0x00    | 0x01    | :x:     | :heavy_check_mark: | :heavy_check_mark: | Channel Fine Tuning |
| 0x00    | 0x02    | :x:     | :heavy_check_mark: | :heavy_check_mark: | Channel Coarse Tuning  |
| 0x00    | 0x03    | :x:     | :x:                | :heavy_check_mark: | Tuning Program Select |
| 0x00    | 0x04    | :x:     | :x:                | :heavy_check_mark: | Tuning Bank Select |
| 0x00    | 0x05    | :x:     | :x:                | :heavy_check_mark: | Modulation Depth Range |
| 0x7F    | 0x7F    | :x:     | :heavy_check_mark: | :heavy_check_mark: | RPN NULL |

## Controllers

| CC\# | Hex  | Vanilla            | Standard           | Full               | Function |
|------|------|--------------------|--------------------|--------------------|----------|
| 0    | 0x00 | :x:                | :heavy_check_mark: | :heavy_check_mark: | Bank Select (MSB) |
| 1    | 0x01 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Modulation Wheel (MSB) |
| 2    | 0x02 | :x:                | :x:                | :heavy_check_mark: | Breath Controller (MSB) |
| 2    | 0x00 |                    |                    |                    | N/A |
| 4    | 0x04 | :x:                | :x:                | :heavy_check_mark: | Foot Controller (MSB) |
| 5    | 0x05 | :x:                | :x:                | :heavy_check_mark: | Portamento Time (MSB) |
| 6    | 0x06 | :x:                | :heavy_check_mark: | :heavy_check_mark: | Data Entry (MSB) |
| 7    | 0x07 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Channel Volume (MSB) |
| 8    | 0x08 | :x:                | :x:                | :heavy_check_mark: | Balance (MSB) |
| 9    | 0x09 |                    |                    |                    | N/A |
| 10   | 0x0A | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Pan (MSB) |
| 11   | 0x0B | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Expression (MSB) |
| 12   | 0x0C | :x:                | :x:                | :heavy_check_mark: | Effect Control 1 (MSB) |
| 13   | 0x0D | :x:                | :x:                | :heavy_check_mark: | Effect Control 2 (MSB) |
| 14   | 0x0E |                    |                    |                    | N/A |
| 15   | 0x0F |                    |                    |                    | N/A |
| 16   | 0x10 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 1 (MSB) |
| 17   | 0x11 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 2 (MSB) |
| 18   | 0x12 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 3 (MSB) |
| 19   | 0x13 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 4 (MSB) |
| 20   | 0x14 |                    |                    |                    | N/A |
| 21   | 0x15 |                    |                    |                    | N/A |
| 22   | 0x16 |                    |                    |                    | N/A |
| 23   | 0x17 |                    |                    |                    | N/A |
| 24   | 0x18 |                    |                    |                    | N/A |
| 25   | 0x19 |                    |                    |                    | N/A |
| 26   | 0x1A |                    |                    |                    | N/A |
| 27   | 0x1B |                    |                    |                    | N/A |
| 28   | 0x1C |                    |                    |                    | N/A |
| 29   | 0x1D |                    |                    |                    | N/A |
| 30   | 0x1E |                    |                    |                    | N/A |
| 31   | 0x1F |                    |                    |                    | N/A |
| 32   | 0x20 | :x:                | :heavy_check_mark: | :heavy_check_mark: | Bank Select (LSB) |
| 33   | 0x21 | :x:                | :x:                | :heavy_check_mark: | Modulation Wheel (LSB) |
| 34   | 0x22 | :x:                | :x:                | :heavy_check_mark: | Breath Controller (LSB) |
| 33   | 0x23 |                    |                    |                    | N/A |
| 36   | 0x24 | :x:                | :x:                | :heavy_check_mark: | Foot Controller (LSB) |
| 37   | 0x25 | :x:                | :x:                | :heavy_check_mark: | Portamento Time (LSB) |
| 38   | 0x26 | :x:                | :heavy_check_mark: | :heavy_check_mark: | Data Entry (LSB) |
| 39   | 0x27 | :x:                | :x:                | :x:                | Channel Volume (LSB) |
| 40   | 0x28 | :x:                | :x:                | :heavy_check_mark: | Balance (LSB) |
| 41   | 0x29 |                    |                    |                    | N/A |
| 42   | 0x2A | :x:                | :x:                | :heavy_check_mark: | Pan (LSB) |
| 43   | 0x2B | :x:                | :x:                | :heavy_check_mark: | Expression (LSB) |
| 44   | 0x2C | :x:                | :x:                | :heavy_check_mark: | Effect Control 1 (LSB) |
| 45   | 0x2D | :x:                | :x:                | :heavy_check_mark: | Effect Control 2 (LSB) |
| 46   | 0x2E |                    |                    |                    | N/A |
| 47   | 0x2F |                    |                    |                    | N/A |
| 48   | 0x30 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 1 (LSB) |
| 49   | 0x31 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 2 (LSB) |
| 50   | 0x32 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 3 (LSB) |
| 51   | 0x33 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 4 (LSB) |
| 52   | 0x34 |                    |                    |                    | N/A |
| 53   | 0x35 |                    |                    |                    | N/A |
| 54   | 0x36 |                    |                    |                    | N/A |
| 55   | 0x37 |                    |                    |                    | N/A |
| 56   | 0x38 |                    |                    |                    | N/A |
| 57   | 0x39 |                    |                    |                    | N/A |
| 58   | 0x3A |                    |                    |                    | N/A |
| 59   | 0x3B |                    |                    |                    | N/A |
| 60   | 0x3C |                    |                    |                    | N/A |
| 61   | 0x3D |                    |                    |                    | N/A |
| 62   | 0x3E |                    |                    |                    | N/A |
| 63   | 0x3F |                    |                    |                    | N/A |
| 64   | 0x40 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Sustain Pedal (Damper, Hold 1) |
| 65   | 0x41 | :x:                | :x:                | :heavy_check_mark: | Portamento On/Off |
| 66   | 0x42 | :x:                | :x:                | :heavy_check_mark: | Sostenuto |
| 67   | 0x43 | :heavy_check_mark: | :warning:[^1]      | :heavy_check_mark: | Soft Pedal |
| 68   | 0x44 | :x:                | :x:                | :heavy_check_mark: | Legato Footswitch |
| 69   | 0x45 | :x:                | :x:                | :heavy_check_mark: | Hold 2 |
| 70   | 0x46 | :x:                | :x:                | :heavy_check_mark: | Sound Controller 1 (Default: Sound Variation) |
| 71   | 0x47 | :x:                | :x:                | :heavy_check_mark: | Sound Controller 2 (Default: Timbre/Harmonic Quality) |
| 72   | 0x48 | :x:                | :x:                | :heavy_check_mark: | Sound Controller 3 (Default: Release Time) |
| 73   | 0x49 | :x:                | :x:                | :heavy_check_mark: | Sound Controller 4 (Default: Attack Time) |
| 74   | 0x4A | :x:                | :x:                | :heavy_check_mark: | Sound Controller 5 (Default: Brightness) |
| 75   | 0x4B | :x:                | :x:                | :heavy_check_mark: | Sound Controller 6 (GM2 Default: Decay Time) |
| 76   | 0x4C | :x:                | :x:                | :heavy_check_mark: | Sound Controller 7 (GM2 Default: Vibrato Rate) |
| 77   | 0x4D | :x:                | :x:                | :heavy_check_mark: | Sound Controller 8 (GM2 Default: Vibrato Depth) |
| 78   | 0x4E | :x:                | :x:                | :heavy_check_mark: | Sound Controller 9 (GM2 Default: Vibrato Delay) |
| 79   | 0x4F | :x:                | :x:                | :heavy_check_mark: | Sound Controller 10 (GM2 Default: Undefined) |
| 80   | 0x50 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 5 |
| 81   | 0x51 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 6 |
| 82   | 0x52 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 7 |
| 83   | 0x53 | :x:                | :x:                | :heavy_check_mark: | General Purpose Controller 8 |
| 84   | 0x54 | :x:                | :x:                | :heavy_check_mark: | Portamento Control |
| 85   | 0x55 |                    |                    |                    | N/A |
| 86   | 0x56 |                    |                    |                    | N/A |
| 87   | 0x57 |                    |                    |                    | N/A |
| 88   | 0x58 | :x:                | :x:                | :heavy_check_mark: | High Resolution Velocity Prefi8|
| 89   | 0x59 |                    |                    |                    | N/A |
| 90   | 0x5A |                    |                    |                    | N/A |
| 91   | 0x5B | :heavy_check_mark: | :warning:[^1]      | :heavy_check_mark: | Effects 1 Depth (Default: Reverb Send Level) |
| 92   | 0x5C | :x:                | :x:                | :heavy_check_mark: | Effects 2 Depth (Default: Tremolo Depth) |
| 93   | 0x5D | :heavy_check_mark: | :warning:[^1]      | :heavy_check_mark: | Effects 3 Depth (Default: Chorus Send Level) |
| 94   | 0x5E | :x:                | :x:                | :heavy_check_mark: | Effects 4 Depth (Default: Celeste \[Detune\] Depth) |
| 95   | 0x5F | :x:                | :x:                | :heavy_check_mark: | Effects 5 Depth (Default: Phaser Depth) |
| 96   | 0x60 | :x:                | :x:                | :heavy_check_mark: | Data Increment |
| 97   | 0x61 | :x:                | :x:                | :heavy_check_mark: | Data Decrement |
| 98   | 0x62 | :x:                | :x:                | :heavy_check_mark: | Non-Registered Parameter Number (LSB) |
| 99   | 0x63 | :x:                | :x:                | :heavy_check_mark: | Non-Registered Parameter Number (MSB) |
| 100  | 0x64 | :x:                | :heavy_check_mark: | :heavy_check_mark: | Registered Parameter Number (LSB) |
| 101  | 0x65 | :x:                | :heavy_check_mark: | :heavy_check_mark: | Registered Parameter Number (MSB) |
| 102  | 0x66 |                    |                    |                    | N/A |
| 103  | 0x67 |                    |                    |                    | N/A |
| 104  | 0x68 |                    |                    |                    | N/A |
| 105  | 0x69 |                    |                    |                    | N/A |
| 106  | 0x6A |                    |                    |                    | N/A |
| 107  | 0x6B |                    |                    |                    | N/A |
| 108  | 0x6C |                    |                    |                    | N/A |
| 109  | 0x6D |                    |                    |                    | N/A |
| 110  | 0x6E | :x:                | :heavy_check_mark: | :heavy_check_mark: | EMIDI: Track Designation |
| 111  | 0x6F | :x:                | :warning:[^2]      | :warning:[^2]      | EMIDI: Track Exclusion / RPG Maker Loop |
| 112  | 0x70 | :x:                | :heavy_check_mark: | :heavy_check_mark: | EMIDI: Program Change |
| 113  | 0x71 | :x:                | :heavy_check_mark: | :heavy_check_mark: | EMIDI: Channel Volume |
| 114  | 0x72 |                    |                    |                    | N/A |
| 115  | 0x73 |                    |                    |                    | N/A |
| 116  | 0x74 | :x:                | :heavy_check_mark: | :heavy_check_mark: | EMIDI: Loop Begin |
| 117  | 0x75 | :x:                | :heavy_check_mark: | :heavy_check_mark: | EMIDI: Loop End |
| 118  | 0x76 | :x:                | :heavy_check_mark: | :heavy_check_mark: | EMIDI: Global Loop Begin |
| 119  | 0x77 | :x:                | :heavy_check_mark: | :heavy_check_mark: | EMIDI: Global Loop End |
| 120  | 0x78 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | All Sound Off |
| 121  | 0x79 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | Reset All Controllers |
| 122  | 0x7A | :x:                | :x:                | :heavy_check_mark: | Local Control On/Off |
| 123  | 0x7B | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | All Notes Off |
| 124  | 0x7C | :x:                | :x:                | :heavy_check_mark: | Omni Mode Off |
| 125  | 0x7D | :x:                | :x:                | :heavy_check_mark: | Omni Mode On |
| 126  | 0x7E | :x:                | :heavy_check_mark: | :heavy_check_mark: | Poly Mode Off (Mono Mode On) |
| 127  | 0x7F | :x:                | :heavy_check_mark: | :heavy_check_mark: | Poly Mode On (Mono Mode Off) |

[^1]: "Soft Pedal" (CC#67), "Reverb Send Level" (CC#91), and "Chorus Send Level" (CC#93) are not supported by Microsoft GS Wavetable Synth.
[^2]: "RPG Maker Loop" conflicts with "EMIDI: Track Exclusion" (CC#111 for both). An RPG Maker loop point will function only if no EMIDI events are found in the MIDI file.
