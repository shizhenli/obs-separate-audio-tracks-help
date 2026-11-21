---
title: "Mac Audio Capture OBS: Fixing a Source That Shows a Meter but Records Silence"
description: "Fix OBS on Mac when the audio meter moves but the recorded file has no source audio. Step-by-step checks for track routing, output settings, and a verification test."
seo_title: "mac audio capture obs: Meter Moves but No Audio in Recording"
seo_description: "Fix OBS on Mac when the audio meter moves but the recorded file has no source audio. Step-by-step checks for track routing, output settings, and a verification test."
keywords:
  - "mac audio capture obs"
date: 2026-11-21T15:05:00+08:00
publishDate: 2026-11-21T15:05:00+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording gameplay and mic on separate tracks in OBS on Mac, and the meter moves but the recorded file has no source audio. This is a track-routing problem, not a capture problem.

## Check Track Assignments First

Open OBS Settings > Output. Under Recording, confirm the recording format and that you are not using a custom output that overrides track selection. Then go to Edit > Advanced Audio Properties. Look at the Tracks column for your game and mic sources. A moving meter means the source is live, but if the wrong track boxes are checked, the file will be silent. For separate tracks, game should be on Track 1 and mic on Track 2, or as you intended. If both are on the same track, or neither is checked, that explains the silence.

## Confirm the Recording Output

In Settings > Output > Recording, check the audio track setting. If it is set to a single track, OBS may write only that track. Set it to the track containing your sources, or use multiple tracks if your editor supports it. On Mac, also verify Settings > Audio > Global Audio Devices does not route your sources to a disabled device.

## Verification Test

Record 10 seconds while speaking and triggering game audio. Stop, then open the file in QuickTime or your editor and inspect each audio track separately. If the meter moved during recording but a track is silent, the track assignment is still wrong. If the correct track now has audio, the fix is confirmed.

## Rollback Note

If you changed multiple settings, revert to your previous Output and Advanced Audio Properties configuration before retesting, so you can isolate which change restored audio. For a controlled diagnosis of your **mac audio capture obs** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
