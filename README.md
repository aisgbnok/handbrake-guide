# HandBrake Guide (Quick and Dirty)

This basic guide provides instructions on how to use HandBrake for converting low-resolution analog and DVD media into modern digital formats.
The guide assumes that your source media is no larger than 1080p and recommends the `Super HQ 1080p30 Surround` preset for such cases.
In this case no modifications are necessary; however, some notable settings are described below.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/images/handbrake-summary-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="/images/handbrake-summary-light.png">
  <img alt="HandBrake Summary Tab" src="/images/handbrake-summary-light.png">
</picture>

## Summary

### Align A/V Start

This setting attempts to correct synchronization issues between audio and video streams.
While generally beneficial, it can occasionally introduce problems in certain cases.
If you encounter A/V desynchronization, try disabling this option to see if it resolves the issue.

## Dimensions

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/images/handbrake-dimensions-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="/images/handbrake-dimensions-light.png">
  <img alt="HandBrake Dimensions Tab" src="/images/handbrake-dimensions-light.png">
</picture>

### Resolution Limit

The `Resolution Limit` setting controls the maximum resolution of the output media.
Disabling this limit ensures that the output media maintains the same resolution as the source media.

## Video

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/images/handbrake-video-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="/images/handbrake-video-light.png">
  <img alt="HandBrake Dimensions Tab" src="/images/handbrake-video-light.png">
</picture>

### Constant Quality (CQ)

The CQ parameter, employing a constant rate factor (CRF) scale, exerts direct control over the quality of the encoded video stream.
Lower CQ values correlate with heightened quality output but necessitate commensurately larger file sizes and extended encoding durations.
Determining the optimal CQ value involves a nuanced trade-off between quality and file size,
often requiring empirical evaluation based on the source material's inherent characteristics and the desired level of fidelity.

While the default value of `18` serves as a reasonable starting point,
an acceptable range typically falls between `16` and `24`.
Within this spectrum, lower values (closer to `16`) prioritize quality at the expense of increased file size,
while higher values (approaching `24`) favor reduced file size with a concomitant reduction in quality.

### Encoder Level

The encoder level defines the range of supported features and capabilities for the encoded video stream.
For 1080p content, an encoder level of `4.0` is typically suffices.
Setting it to `Auto` allows the encoder to select the optimal level based on the source video.

### Encoder Tune

The `Encoder Tune` setting adjusts the encoder's settings to optimize the output for specific types of source content.
The default setting of `None` is generally sufficient.
However, for home video films, setting it to `Film` or `Grain` may improve the output quality.

- **Film:**
  Real life footage, films etc may benefit. (Not Cartoons or Anime).
  Typically won't do any harm to if left on for most content.

- **Grain:**
  Typically used for very grainy or old content.

> [!NOTE]  
> Before deciding to change from `None`,
> it's recommended to test the output with different settings to determine the best quality for your media.

For more information,
refer to the [HandBrake Documentation: x264 Presets and Tunes](https://handbrake.fr/docs/en/1.2.0/technical/video-x264-presets-tunes.html).

## Audio

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/images/handbrake-audio-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="/images/handbrake-audio-light.png">
  <img alt="HandBrake Dimensions Tab" src="/images/handbrake-audio-light.png">
</picture>

HandBrake's default audio configuration is generally appropriate for the majority of use cases,
encompassing surround sound configurations.
For 1080p content, an audio bitrate of 160 kbps strikes a balance between fidelity and file size efficiency.
Nonetheless, contingent upon the specific audio characteristics and desired level of auditory fidelity,
adjustments to the bitrate may be warranted.