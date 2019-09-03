# Innocent

We are given `pcapng` file. These types of files should be open in `Wireshark`. 

There are about 85 packets. Inspecting the protocol we can see there are TCP and HTTP. Usually when we see HTTP, we can dump all HTTP objects.

To dump all HTTP objects: -

`File` -> `Export Objects` -> `HTTP` -> Save All

There are 2 files of interest.

1. The `alert.png` which says Base64 Encode and Decode.
2. The `nothing%20is%20here.txt` file.

Inspect the contents of the .txt file. It says `YXB1Ym9oMjAxOXtlQHN5X2h1aD99`. With the hint from alert.png, it is safe to assume that it is Base64 encoded.

#### Flag

Flag `apuboh2019{e@sy_huh?}`
