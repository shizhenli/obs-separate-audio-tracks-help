---
title: "Desktop Audio Mac OBS: Meter Moves but Recording Has No Source Audio"
description: "Fix OBS on Mac when the desktop audio meter moves but the recorded file has no source audio. Step-by-step checks for track assignment, monitoring, and a verification test."
seo_title: "Desktop Audio Mac OBS: Meter Moves but No Recorded Audio"
seo_description: "Fix OBS on Mac when the desktop audio meter moves but the recorded file has no source audio. Step-by-step checks for track assignment, monitoring, and a verification test."
keywords:
  - "desktop audio mac obs"
date: 2026-11-21T15:01:46+08:00
publishDate: 2026-11-21T15:01:46+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You're recording a game and mic on separate tracks in OBS on Mac, and the desktop audio meter moves, but the recorded file has no source audio. Let's diagnose this controlled, one step at a time.

## Check the source's track assignment

Open the Advanced Audio Properties for the desktop audio source. Confirm at least one track is checked for recording, and note which number. Then check Settings > Output > Recording and verify the track list includes that number. If the source's track is unchecked, the meter still moves but nothing is written to the file. Result interpretation: if no track is checked, that's your cause; enable one and re-test.

## Check monitoring and output routing

In Advanced Audio Properties, set the desktop audio source to Monitor Off unless you need to hear it. On Mac, a source set to Monitor and Output can behave unexpectedly with some output devices. Also confirm the recording path is local and not a stream-only output.

## Verify with a short test recording

Record 15 seconds with the game audio playing. Stop, then open the file in a player that shows track selection. If the file has multiple tracks, switch to the track you assigned. If the meter moved but the file is silent on every track, the source is not being captured into the recording pipeline. If only one track is silent, the track assignment is wrong.

## Rollback and recovery

Before changing more settings, export your current profile and scene collection. If a change makes things worse, re-import the backup. Keep a known-good profile for separate-track recordings.

If the meter still moves but the file has no source audio after these checks, this is a **desktop audio mac obs** routing issue that needs a closer look at your device and output configuration.

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your OBS logs and a short test file.
