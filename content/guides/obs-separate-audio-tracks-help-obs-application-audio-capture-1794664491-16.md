---
title: "OBS Application Audio Capture: Meter Moves but No Source Audio in Recording"
description: "Fix OBS application audio capture when the meter moves but the recording has no source audio. Step-by-step checks for track routing, source selection, and verification."
seo_title: "OBS Application Audio Capture: Meter Moves but No Source Audio"
seo_description: "Fix OBS application audio capture when the meter moves but the recording has no source audio. Step-by-step checks for track routing, source selection, and verification."
keywords:
  - "obs application audio capture"
date: 2026-11-22T11:02:42+08:00
publishDate: 2026-11-22T11:02:42+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and at the audio source is not captured step the meter moves but the recorded file has no source audio. That points to a routing or source-mapping issue, not a dead capture device. Let's diagnose it in order.

## Check the source assignment in the recording track

Open the advanced audio properties for your application audio capture source. Confirm the source is assigned to a track that is actually written to the file. In many setups, only track 1 is recorded by default. If your source is checked on track 2 but track 2 is not enabled in output settings, the meter will still move because monitoring is live, but the file will contain silence on that track. Enable the correct track in Settings > Output > Recording and re-check the source's track boxes.

## Confirm the correct window is selected

For **obs application audio capture**, the source must point to the exact executable or window that is producing sound. If you selected a launcher or a different process, the meter may move from system audio while the intended app is not captured. Switch the source to the specific game process, then play a known sound and watch the meter.

## Run a verification test

Record 10 seconds with a constant sound from the app. Stop, then open the file in a player that shows track selection. If track 1 has audio and track 2 is empty, your track routing is still wrong. If both are empty, the source is not the active process.

## Rollback and recovery

If a change makes things worse, revert the track checkboxes and output settings to their previous state before testing again. Keep a backup of your scene collection so you can restore it.

If the meter still moves but the file stays silent after these checks,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your track layout and source list.
