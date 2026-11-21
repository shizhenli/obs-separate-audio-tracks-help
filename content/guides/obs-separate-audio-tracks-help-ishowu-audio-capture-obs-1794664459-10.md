---
title: "iShowU Audio Capture in OBS: Why the Meter Moves but the Recording Is Silent"
description: "Fix iShowU Audio Capture in OBS when the meter moves but the recorded file has no source audio. Step-by-step checks, verification test, and rollback note."
seo_title: "iShowU Audio Capture OBS: Meter Moves but No Recorded Audio Fix"
seo_description: "Fix iShowU Audio Capture in OBS when the meter moves but the recorded file has no source audio. Step-by-step checks, verification test, and rollback note."
keywords:
  - "ishowu audio capture obs"
date: 2026-11-21T15:05:00+08:00
publishDate: 2026-11-21T15:05:00+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and your mic on separate tracks in OBS, and at the audio source step the iShowU meter moves, but the saved file has no source audio. This is a routing problem, not a level problem, so work through the checks below in order and note the exact result each time.

## Check the source assignment and track

Open the Advanced Audio Properties window and confirm the iShowU source has a checkmark under the track you intend to record, not only under Monitor. Then open Settings, Output, and confirm the recording track selection matches that same track number. If the source is checked on Track 2 but the output records Track 1, the meter will still move while the file stays silent. Result to expect: the source and output track numbers match exactly.

## Check the macOS routing

In macOS Sound settings, confirm the output device is the Multi-Output Device that includes iShowU, not the raw iShowU device alone. If OBS receives iShowU directly while system audio goes elsewhere, the meter can show activity from a partial route. Result to expect: the same Multi-Output Device is selected for system output and visible to OBS.

## Run a verification test

Record 15 seconds with a known sound, then play the file in a player that shows per-track audio. If the track is silent, switch the iShowU source to Track 1 only, record again, and compare. This isolates whether the fault is the track map or the capture route.

## Rollback and recovery

Before changing more settings, export your current OBS profile so you can restore it. If a test makes things worse, reimport that profile and return to the last working configuration.

If the meter still moves while the file stays silent after these checks,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your track map and macOS routing details. For **ishowu audio capture obs** setups, confirm the source and output track numbers match before anything else.
