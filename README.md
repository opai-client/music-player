# music-player
A music player.

## This extension uses services provided by the NetEase Cloud Music platform from China. Other regions *may* experience network issues.

## Shortcut Keys
- `Shift + Right Arrow`: Fast forward to the beginning of the next line
- `Shift + Left Arrow`: Rewind to the beginning of the previous line
- `Space`: Pause / Resume
- `Right Arrow`: Fast forward 5 sec
- `Left Arrow`: Rewind 5 sec

## Screenshots

![sc1](https://github.com/user-attachments/assets/9174fb29-aef4-48e9-a6e6-9285e4a87c12)

![sc2](https://github.com/user-attachments/assets/b6ac8ab4-c7cf-4c8b-ac9a-2f8576147a39)

## Showcase
https://github.com/user-attachments/assets/4ec7f442-471c-4263-bde0-c4bd045dada4
___

## Why is this extension SO BIG?
### File structure:
### NCM.jar/
- fonts/
  - pf.ttf (~10MB)
  - pfBold.ttf (~10MB)
- ncmapi.exe (A local node.js api for NetEase Cloud Music, ~65MB)
- unblockneteasemusic.exe (A local node.js http proxy for unlocking member songs, ~36MB)

### If you are afraid that the executable file provided in the extension contains a virus, you can compile one yourself and rename it to the same name and put it in the .jar.
- [ncmapi (npm)](https://www.npmjs.com/package/NeteaseCloudMusicApi)
  - You need to manually add the http proxy to the source code. In util/request.js, add `options.proxy = "http://127.0.0.1:8080"` before the `if (options.proxy) {` code. Follow the tutorial to build the project. Finally, run `pkg .` in the command prompt in the project root directory to build the executable file.
- [UnblockNeteaseMusic/server (github)](https://github.com/UnblockNeteaseMusic/server)
  - Download the latest release or build one yourself.
