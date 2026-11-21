---
title: "iShowU Audio Capture on OBS Mac: Meter Moves but No Source Audio in Recording"
description: "Fix iShowU Audio Capture on OBS Mac when the meter moves but the recorded file has no source audio. Step-by-step diagnosis and verification."
seo_title: "iShowU Audio Capture OBS Mac: Fix Meter Moves but No Audio"
seo_description: "Fix iShowU Audio Capture on OBS Mac when the meter moves but the recorded file has no source audio. Step-by-step diagnosis and verification."
keywords:
  - "ishowu audio capture obs mac"
date: 2026-11-21T15:05:00+08:00
publishDate: 2026-11-21T15:05:00+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording game and mic on separate tracks in OBS on Mac, but at the audio source is not captured step the meter moves while the recorded file has no source audio.

## Check the Source Assignment

Open OBS Settings > Audio and confirm the iShowU device is selected where you expect it. Then check the mixer: click the gear next to the iShowU source and open Advanced Audio Properties. Verify the source is assigned to a track that is actually enabled in Settings > Output > Recording. A common cause is the source routed only to Track 2 while only Track 1 is recorded.

## Check macOS Permissions

Go to System Settings > Privacy & Security > Screen Recording and confirm OBS is enabled. Then check Microphone permission for OBS. If iShowU is a virtual device, also confirm it appears in Audio MIDI Setup and is not muted there. If the meter moves in OBS but the file is silent, the source may be monitored but not routed to the recording track.

## Verification Test

Record a 10-second clip with both sources active. Stop recording, then open the file in QuickTime or import it into OBS. Play it back and watch the audio meter. If the track is silent, recheck Advanced Audio Properties and enable the correct track for that source. If the track now has audio, the routing was the issue.

## Rollback and Recovery

If you changed track assignments, note the original layout before saving. To recover, reopen Advanced Audio Properties and restore each source to its previous track, then re-record a short test. Avoid deleting the original recording until you confirm the new file has audio.

If the meter still moves but the file stays silent after these checks, the issue may be a conflict between **iShowU audio capture obs mac** routing and OBS track settings.

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your OBS audio settings and a short test recording.
