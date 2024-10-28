# The Vault

The vault is a collection of my ideas, plans and project descriptions that I would like to tackle at some point.
Some of my more eccentric ideas and projects will be kept private until the time is right for these reasons:

1. Some might be controversial
2. Some people in power might not like the potential outcomes of the projects
3. They might result in death or injury in their infancy
4. Chaos is a pre-requisite
5. Chaos is the outcome

Previously The Vault was a collection of documents loosely structured, so I will be updating this README every now and then with an index and slowly migrate everything here.

# Index

## Dim
Project link: [https://github.com/Dusk-Labs/dim](https://github.com/Dusk-Labs/dim)

Alternative to jellyfin aiming for the same level of polish as plex and just as much device support.
Some innovative features are being cooked such as:
1. No transcoding when displaying bitmap subtitles
2. More efficient transcoding
3. On-the-fly subtitle streaming
4. Low time to video output latency

### Status
Project is currently paused until I save enough funds to sponsor bug and feature bounties.

## Nightfall v2
Project link: [https://github.com/Dusk-Labs/nightfall](https://github.com/Dusk-Labs/nightfall)

High performance real-time transcoding engine. Nightfall v1 is totally usable but is not better than the competition.
Feature I will be focusing on:

1. Ability to transcode one stream to another without having to worry about hardware features (unless you want to)
2. Introspection into the state of the stream via events (crashes, errors, format incompatibilities, broken file, progress)
3. Ability to multiplex multiple streams without having to fallback to manual command line. (ie: transcode video to file and also spit out i-frames to stdout)
4. Better DX for writing complex filter-graphs. Ideally some rust-like syntax or infernal-like graph builder.
5. Efficient stream throttling (by cpu or frame-rate)
6. Ability to pause / unpause transcode either remotely or via on-event handlers.
7. Abstractions for creating on-demand video streams (lazy transcoding)
8. Abstractions for tuning a video for specific platforms
9. One-line abstraction that can do video fidelity scoring automatically and emit the info as an event.
10. Ideally some level of type safe abstractions that can eliminate invalid command combinations, but without sacrificing documentation.
11. Work around incompatible encoders / decoders with fallbacks, automatically (but ideally opt-in??)
12. Export stream state and errors to a standard format that can be easily distributed.
13. Make it easy to negotiate video stream encoding.
14. Extract assets in a streaming fashion or completely on demand or while encoding a video.

Eventually I want nightfall to be a self-contained library with most ffmpeg-related stuff being statically linked in and the questionably licensed modules dynamically linked or provided by the system.
For now we will have to work with the ffmpeg binary directly, which sadly limits our flexibility, but will be okay for most stuff.

### Status
In-Progress, tune in for more details in ~1 month.

## KinoStick v1
More Details: [./kinostick/README.md](./kinostick/README.md)

Are you sad about the discontinuation of Google Chromecast? Do you think that current TV boxes are doing too much? Why the fuck do I want to play video games on my TV? Ever struggled to stream files to your TV in their original quality while youre friends are staring at you like a lunatic?

This project is for you.

A low cost (sub 30$) device optimizied for doing just one thing and doing it well, streaming video. The details are a bit loose but it will likely be a simple device using the RK3328 chip, running a very slimmed down linux distro (sub 100mb) and a GUI built with slint.

Target features:
1. Low cost (sub 30$)
2. Support for most containers and video formats with hardware decode support and software fallback
3. Support for high-bitrate content (think 200gb remuxes)
4. Boot-times at least under 4s.
5. Chromecast and Airplay compatibility
6. Optional path towards device certification for DRM (Yes, I know. That said I have friends, and they sometimes want to watch netflix. You can use the FLOSS version if you dont like this)

### Status
In ideation and prototyping phase.
