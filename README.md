# Handbrake Guide (Quick and Dirty)

This is a quick and dirty handbrake guide for transcoding low-resolution analog and DVD media into modern digital formats.

Assuming your source media is no larger than 1080p, the `Super HQ 1080p30 Surround` preset should suffice.
In this case no modifications are necessary; however, some notable settings are described below.


## Summary

### Align A/V Start

If you encounter issues with audio/video synchronization, consider disabling the Align A/V Start option.
This can help resolve any syncing problems.

## Dimensions

### Resolution Limit

Turning off the resolution limit will ensure the output media is the same resolution as the source media.

## Video

### Constant Constant Quality (CQ)

This setting adjusts the quality of the output.
A smaller number means higher quality, but also a larger file size and longer encoding time.

### Encoder Level

If your video is not larger than 1080p, an encoder level of `4.0` is standard.
Setting it to `Auto` will ensure it is not limited.

### Encoder Tune

The default setting of `None` is sufficient.
However, for home video films, setting it to `Film` or `Grain` may be beneficial.

- **Film:** Real life footage, films etc may benefit. (Not Cartoons or Anime).
  Typically won’t do any harm to if left on for most content.
- **Grain:** Typically used for very grainy or old content.

> [!NOTE]  
> Before deciding to change from `None` test the output with different settings to determine the best quality for your media.

See the [HandBrake Documentation: x264 Presets and Tunes](https://handbrake.fr/docs/en/1.2.0/technical/video-x264-presets-tunes.html).

## Audio

The default settings in the Audio tab should be fine for most purposes and account for surround sound.
For 1080p, an audio bitrate of 160 is adequate.