---
title: "OBS Audio Input Capture: Meter Moves but the Recording Has No Source Audio"
description: "Fix OBS audio input capture when the meter moves but the recording has no source audio. Step-by-step checks for track routing, monitoring, and verification."
seo_title: "OBS Audio Input Capture: Meter Moves but No Source Audio Recorded"
seo_description: "Fix OBS audio input capture when the meter moves but the recording has no source audio. Step-by-step checks for track routing, monitoring, and verification."
keywords:
  - "obs audio input capture"
date: 2026-11-24T08:02:38+08:00
publishDate: 2026-11-24T08:02:38+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording game and mic on separate tracks, and at the audio source is not captured step the meter moves but the recorded file has no source audio.

## Check Track Routing First

Open the Advanced Audio Properties for the source. Confirm the source is assigned to the track you expect, and that the track is enabled in Settings > Output > Recording. A meter can move while the source is routed to a track that is not written to the file. If the source is on track 2 but only track 1 is enabled, the file will be silent for that source.

## Check Monitoring and Output

In Advanced Audio Properties, verify the source is not set to Monitor Only. Monitor Only lets you hear the source but does not send it to the recording. Set it to Monitor and Output, or Monitor Off, depending on your needs. Also confirm the source is not muted and that its volume is not at zero.

## Check the Recording Format

If you record to a format that does not support multiple tracks, such as some streaming formats, the extra tracks may be dropped. Use MKV or MP4 with multiple audio tracks enabled. Then check the file in a player that lets you select audio tracks.

## Verification Test

Record a short clip while speaking and playing game audio. Stop recording, open the file in a player, and switch between audio tracks. Each track should contain only its assigned source. If a track is silent, return to Advanced Audio Properties and confirm the track assignment and the enabled tracks in Output settings.

## Rollback and Recovery

If you changed track assignments, note the original settings before reverting. If a recording is already silent, the missing audio cannot be recovered from the file; re-record after fixing the routing. For a controlled diagnosis of your **obs audio input capture** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
