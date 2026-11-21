---
title: "Capture Audio OBS Mac: When the Meter Moves but the Recording Is Silent"
description: "Fix OBS on Mac when the audio meter moves but the recording has no source audio. Step-by-step checks for track routing, monitoring, and verification."
seo_title: "Capture Audio OBS Mac: Fix Meter Moves but No Source Audio"
seo_description: "Fix OBS on Mac when the audio meter moves but the recording has no source audio. Step-by-step checks for track routing, monitoring, and verification."
keywords:
  - "capture audio obs mac"
date: 2026-11-21T14:58:41+08:00
publishDate: 2026-11-21T14:58:41+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You're recording gameplay and mic on separate tracks in OBS on Mac, and although the meter moves during recording, the file has no source audio. This happens at the "audio source is not captured" step, before you've completed a controlled diagnosis. Let's fix that specific failure.

## Check Track Assignments

Open OBS Settings > Output. Under Recording, confirm the recording format is MKV or MOV (not MP4) and that Audio Track 1 is selected. Then go to Edit > Advanced Audio Properties. For each source (game and mic), verify the checkboxes under Tracks. A source must be checked on at least one track that is also enabled in Output settings. If a source is only checked on Track 2 but Track 2 is not enabled for recording, the meter will move but the file will be silent. Enable the correct tracks and re-test.

## Verify Monitoring and Output

In Advanced Audio Properties, set Monitoring to "Monitor Off" for all sources to avoid feedback. Then check that the correct output device is selected in Settings > Audio. On Mac, ensure the device is not set to "Default" if you have multiple interfaces. Also, confirm that no source is muted (speaker icon) and that the fader is up.

## Run a Verification Test

Record a 10-second clip while speaking and playing game audio. Stop recording and open the file in QuickTime or a media player. If you still hear nothing, export the audio tracks separately using a tool like Audacity to inspect each track. This confirms whether the issue is track routing or source capture.

## Rollback and Recovery

If you changed track assignments and the problem persists, revert to the last working configuration by resetting OBS audio settings to default (Settings > Audio > Reset). Then reapply changes one at a time. For persistent **capture audio obs mac** issues,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your OBS logs and a sample file.
