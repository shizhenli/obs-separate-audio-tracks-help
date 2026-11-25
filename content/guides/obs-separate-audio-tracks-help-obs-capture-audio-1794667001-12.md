---
title: "OBS Capture Audio: When the Meter Moves but the Recording Is Silent"
description: "Fix OBS capture audio when the meter moves but the recording has no source audio. Check track assignments, monitoring, and encoder settings with a controlled test."
seo_title: "OBS Capture Audio: Meter Moves but Recording Has No Sound"
seo_description: "Fix OBS capture audio when the meter moves but the recording has no source audio. Check track assignments, monitoring, and encoder settings with a controlled test."
keywords:
  - "obs capture audio"
date: 2026-11-25T12:02:38+08:00
publishDate: 2026-11-25T12:02:38+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, the meter moves, but the saved file has no source audio.

## Confirm the track is actually being written

Open Settings > Output > Recording and note the recording format. In the Audio Mixer, click the gear next to the silent source and open Advanced Audio Properties. Check which track numbers are enabled for that source. If only track 1 is checked but your player reads track 2, the file will appear silent. Enable the intended track and record a short clip.

## Check the encoder and container

If you record to a format that does not carry multiple tracks, OBS may write only one. Switch to mkv or mov for multi-track work, then remux to mp4 afterward if needed. Record ten seconds and inspect the file in a player that lets you select audio tracks. If the source appears on the expected track, the capture path is working.

## Run a verification test

Create a fresh scene with one source, set it to track 1 only, and record while speaking or playing. Stop, open the file, and confirm the waveform is present. If it is, add the second source on track 2 and repeat. This isolates whether the problem is the source or the track mapping.

## Recovery note

Before changing settings, export your current profile so you can restore it. If a test makes things worse, reimport that profile and return to the last known-good configuration.

If the meter still moves while the file stays silent after these checks, the issue is likely in how **obs capture audio** is routed rather than the source itself.

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your log file and a sample recording.
