---
title: "OBS Multi-Track Recording Is Silent: Fixing a Silent Source on One Track"
description: "Troubleshoot OBS multi-track recordings where tracks exist but one source is silent or out of sync. Step-by-step checks and a verification test."
seo_title: "OBS Multi-Track Recording Silent: Fix a Silent Source Track"
seo_description: "Troubleshoot OBS multi-track recordings where tracks exist but one source is silent or out of sync. Step-by-step checks and a verification test."
keywords:
  - "obs audio not recording"
date: 2026-11-24T09:02:38+08:00
publishDate: 2026-11-24T09:02:38+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You're recording game and mic on separate tracks in OBS, but when you open the file, one track is silent or out of sync.

## Check the source routing first

Open OBS and go to the mixer. Confirm the silent source shows movement on its meter while you speak or play. If the meter moves, the source is live; the problem is in track assignment or the recording path. Click the gear next to the source, choose Advanced Audio Properties, and verify the source has a checkmark under the track you expect. A common cause of **obs audio not recording** on the intended track is a source assigned to Track 1 only while you review Track 2. Also confirm the track number you assigned matches the track you inspect in your editor.

## Check sync and format

If the track has audio but drifts out of sync, note whether the offset grows over time. A constant offset suggests a sample-rate mismatch. Set OBS and your editor to the same rate, typically 48 kHz. A growing offset often points to a device or buffer issue; reconnect the audio device and restart OBS.

## Verification test

Record 20 seconds: count aloud while the game plays. Stop, open the file in an editor that shows tracks separately, and inspect each track. Expected result: your voice appears only on the mic track, game audio only on the game track, and both align with the visual count. If a track is still silent, recheck Advanced Audio Properties and the track number in the editor.

## Rollback and recovery

Before changing more settings, duplicate your scene collection or export a backup. If a change makes things worse, restore the backup and reapply one adjustment at a time. If the silent track persists after these checks,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your OBS log and a short test recording.
