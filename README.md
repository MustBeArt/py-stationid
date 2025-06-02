# py-stationid
Python encode/decode of station ID for Opulent Voice

## Testing from command line

```sh
% python3 callsign_encode.py KB5MU
Encoded callsign: 0x00000341ca5b
Decoded callsign: KB5MU
%
```

## Testing from REPL
```
% python3
Python 3.13.2 (main, Feb  4 2025, 14:51:09) [Clang 16.0.0 (clang-1600.0.26.6)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> from callsign_encode import encode_callsign, decode_callsign
>>> encode_callsign("KB5MU")
54643291
>>> decode_callsign(_)
'KB5MU'
>>> encode_callsign("ABCDEFGHI")
60322419460881
>>> encode_callsign("ABCDEFGHIJ")
Traceback (most recent call last):
  File "<python-input-7>", line 1, in <module>
    encode_callsign("ABCDEFGHIJ")
    ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^
  File "/Users/kb5mu/Desktop/callsign_encode.py", line 32, in encode_callsign
    raise ValueError("Encoded callsign exceeds maximum length of 6 bytes.")
ValueError: Encoded callsign exceeds maximum length of 6 bytes.
>>> 
```
