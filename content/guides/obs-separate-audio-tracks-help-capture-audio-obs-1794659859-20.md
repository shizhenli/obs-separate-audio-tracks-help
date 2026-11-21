---
title: "OBS Audio Source Not Captured: When the Meter Moves but the Recording Is Silent"
description: "Fix OBS when the audio meter moves but the recorded file has no source audio. Step-by-step checks for track assignment, monitoring, and output routing."
seo_title: "OBS Audio Source Not Captured: Meter Moves, Recording Silent"
seo_description: "Fix OBS when the audio meter moves but the recorded file has no source audio. Step-by-step checks for track assignment, monitoring, and output routing."
keywords:
  - "capture audio obs"
date: 2026-11-21T14:58:41+08:00
publishDate: 2026-11-21T14:58:41+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You're recording game and mic on separate tracks, the meter bounces, but the file plays back with no source audio. Let's work through this in order.

## Check the track assignment first
Open Settings > Output, set Recording to Advanced, then open the Audio tab. Confirm each source has a checkmark in the track you expect. A moving meter only proves the source is live; it does not prove the source is assigned to a recorded track. If the game is on track 2 and the mic on track 3, both boxes must be ticked. Untick and retick each one to force a refresh.

## Confirm the source is not monitor-only
In the Audio Mixer, click the gear next to the silent source and open Advanced Audio Properties. Check that the source is not set to Monitor Off with output muted. Set it to Monitor and Output for a quick test. If the meter still moves but the file is silent, the problem is downstream, not in the source.

## Verify with a short test recording
Record ten seconds while speaking and playing game audio. Stop, then open the file in a player that shows track selection, such as VLC under Audio > Audio Track. If track 1 is silent but track 2 has audio, your track mapping is wrong. If every track is silent, revisit the output settings above.

## Rollback and recovery
If a recent change caused this, restore your previous scene collection via Scene Collection > Import, or revert the last output settings change. Keep a backup of your scene collection before further edits.

If the meter still moves while the file stays silent, this is the point to stop guessing;

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your log file and a sample recording so the **capture audio obs** path can be checked properly.
