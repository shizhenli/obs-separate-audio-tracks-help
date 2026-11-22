---
title: "OBS Recording Has No Source Audio: When the Meter Moves but the Track Is Silent"
description: "Fix OBS recordings where the meter moves but the file has no source audio. Check track assignment, advanced audio settings, and verify with a short test recording."
seo_title: "No Audio on OBS Recording: Fix a Silent Source Track"
seo_description: "Fix OBS recordings where the meter moves but the file has no source audio. Check track assignment, advanced audio settings, and verify with a short test recording."
keywords:
  - "no audio on obs recording"
date: 2026-11-22T10:02:40+08:00
publishDate: 2026-11-22T10:02:40+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

## Troubleshooting

You are recording a game and mic on separate tracks, the meter moves, but the saved file has no source audio. Start by opening Settings > Output and confirming the recording mode is set to Advanced, not Simple. In Simple mode, OBS ignores per-source track assignments, so a source can meter normally while never reaching the file. Next, open Edit > Advanced Audio Properties. For each source you expect to hear, check the Track column. A source with only Track 1 enabled will not appear on Tracks 2 or 3, and some editors and players default to a single track. Enable the track you actually want, then confirm the recording format. MKV and MOV preserve multiple tracks reliably; MP4 can behave inconsistently if recording stops unexpectedly. If you recently changed the output mode or track layout, roll back to the previous profile via Profile > Manage Profiles before retesting, so you compare like with like. Now run a verification test: record ten seconds while speaking and playing game audio, stop normally, and open the file in a player that lets you select audio tracks, such as VLC under Audio > Audio Track. If the source appears on one track but not another, the problem is track assignment, not capture. If every track is silent, recheck that the source is not muted and that its volume is above zero in Advanced Audio Properties. This controlled check isolates whether you are facing **no audio on obs recording** at the track level or at the source level. If the test still fails,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your output mode, track layout, and container format.
