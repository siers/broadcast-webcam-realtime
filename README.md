check out nixos-module.nix, which serves index.html, which loads hls.js which connects to the rtmp nginx module, which is fed by ffmpeg in the background and creates 1. m3u8 playlist and the ts files, which get deleted when they're outdated

adding these settings to ffmpeg for encoding was required to make this work on android

```
  -pix_fmt yuv420p \
  -profile:v baseline \
```
