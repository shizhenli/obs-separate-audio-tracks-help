---
title: "OBS Audio Application Capture: When the Meter Moves but the Recording Has No Source Audio"
description: "Fix OBS audio application capture when the meter moves but the recorded file has no source audio. Step-by-step checks for Windows, macOS, and multi-track recordings."
seo_title: "OBS Audio Application Capture: Meter Moves, No Recorded Audio"
seo_description: "Fix OBS audio application capture when the meter moves but the recorded file has no source audio. Step-by-step checks for Windows, macOS, and multi-track recordings."
keywords:
  - "obs audio application capture"
date: 2026-11-22T12:02:53+08:00
publishDate: 2026-11-22T12:02:53+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and OBS shows a moving meter for your application source, but the recorded file contains no audio from that source. This is a track-routing problem, not a capture problem, and the checks below isolate it before you change anything else.

## Confirm the source is actually assigned to a track

Open the Advanced Audio Properties window (the gear icon next to the Audio Mixer). Find the application source row and look at the Track columns. At least one track box must be checked. If every box is empty, the meter still moves because OBS is monitoring the source, but nothing is written to the file. Check Track 2 or higher if Track 1 is reserved for your mic. Click OK, then record a ten-second test.

## Check the recording track selection

Go to Settings > Output > Recording. In the Recording Track field, confirm the selected track matches the track you enabled for the application source. If the field says Track 1 and your game audio is only on Track 2, the file will be silent for that source. Set it to the correct track or leave it on the multi-track option your container supports.

## Verify the container and codec

If you record to a format that does not preserve multiple tracks, such as some FLV configurations, switch the recording format to MKV or MP4. Then re-test.

## Verification test

Record fifteen seconds with the game audible. Stop, open the file in a player that shows track selection, and confirm the application source appears on its assigned track. If it does, the fix is complete.

## Rollback note

If the test file is still silent, revert the track assignments you changed and return to the previous settings before trying a different output mode, so you can compare results cleanly. For a guided diagnosis of your **obs audio application capture** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
