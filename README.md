# IMPORTANT NOTICE
This project is discontinued. Please visit [https://github.com/EraserKing/CloudMusicGear] and switch to the new tool.

# Unblock163MusicClient

Unblock 163 Cloud Music Windows client.

Acts as a proxy.

Didn't do much about this, but just to prove it works!

When you access song / album / artist / playlist page, or search result, you should find the disabled songs return to enabled.

## Usage

1. Run and it listens at port 3412 (default).
2. Open Windows client, set proxy to IP 127.0.0.1, port 3412.
3. Save and restart the client.
4. Enjoy!

## Command line arugments

`/port` : specify the port it listens at. **Example**: `/port 3456`

`/verbose`: turn on verbose log.

`/overseas`: turn on overseas mode (not tested yet). *Not recommended for Mainland China users.*

`/overseasproxy`: assign a reverse proxy for overseas users. *This should be used when the default overseas mode is not working.* **`/overseas` must be turned on first.** **Example**: `/overseasproxy 14.215.9.16`

Available proxys are `14.215.9.16, 14.215.9.43, 219.138.27.16, 219.138.27.67, 163.177.171.13, 163.177.171.14, 163.177.171.16, 163.177.171.17, 163.177.171.18, 163.177.171.19, 163.177.171.20, 163.177.171.21, 163.177.171.22, 163.177.171.28, 163.177.171.29, 163.177.171.31, 163.177.171.32, 163.177.171.33, 163.177.171.34, 163.177.171.35, 163.177.171.37, 163.177.171.175, 163.177.171.206`.

`/playbackbitrate`: override the playback bitrate specified in the client. **Accepted values**: `96000`, `128000`, `192000`, `320000`. **Example**: `/playbackbitrate 320000`

`/downloadbitrate`: override the download bitrate specified in the client. **Accepted values**: `96000`, `128000`, `192000`, `320000`. **Example**: `/downloadbitrate 320000`

## Download

See [https://github.com/EraserKing/Unblock163MusicClient/releases]

## Known issues

1. Download is working, but if you just specify download quality to 320k, you may find during downloading the quality returns to 128k. This cannot be solved, but it's **strongly recommended to override the download bitrate to 320k** via command line arguments `/downloadbitrate 320000`.
2. The settings playback music quality won't take effect immediately after you change them; instead it will only be switched properly after it meets a normal song (not disabled). **You could use command line arguments to override this!**

## Open issues

Please report the following information:

* Operating system
* Song / Album / Playlist name (how I can locate to that song)
* Whether the issue happens on specific songs, or all songs
* Whether it can be reproduced on web client for the same song

## Building

Need the following packages:

FiddlerCore [http://www.telerik.com/fiddler/fiddlercore]

Newtonsoft.Json 6.0.8 [https://github.com/JamesNK/Newtonsoft.Json]

Under Visual Studio 2015.

## Thanks

Thanks yanunon for his API analysis! [https://github.com/yanunon/NeteaseCloudMusic]
