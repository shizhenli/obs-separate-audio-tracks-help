---
title: "Desktop Audio in OBS: Meter Moves but Recording Has No Source Audio"
description: "Fix desktop audio in OBS when the meter moves but the recorded file has no source audio. Step-by-step checks for track assignment, monitoring, and output routing."
seo_title: "Desktop Audio in OBS: Meter Moves but No Recorded Audio"
seo_description: "Fix desktop audio in OBS when the meter moves but the recorded file has no source audio. Step-by-step checks for track assignment, monitoring, and output routing."
keywords:
  - "desktop audio in obs"
date: 2026-11-21T15:01:46+08:00
publishDate: 2026-11-21T15:01:46+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and the desktop audio meter moves, but the recorded file has no source audio. Let's isolate the cause before changing anything else.

## Check Track Assignment First

Open the Advanced Audio Properties for your desktop audio source. Confirm at least one track is checked under Tracks. If none are checked, the meter still moves because the source is live, but nothing is written to the file. Check Track 1 or the track you use for desktop audio, then apply.

## Verify the Recording Output

In Settings > Output, confirm the recording path and that the output mode matches your setup (Simple or Advanced). In Advanced mode, ensure the recording track selection includes the track you assigned. If you use multiple tracks, note which track holds desktop audio; a player that only reads Track 1 will appear silent if desktop audio is on Track 2.

## Test with a Short Recording

Record 10 seconds of game audio with the mic muted. Stop, then open the file in a player that lets you select audio tracks. If Track 1 is silent but Track 2 has audio, the source is captured correctly and the issue is track selection in playback or export. If all tracks are silent, return to Advanced Audio Properties and recheck the track boxes.

## Rollback Note

If you changed track assignments and the result is worse, revert to your previous track layout before continuing. Keep a note of which track held desktop audio so you can restore it.

If the meter still moves but the file has no source audio after these checks, the issue may be in output routing or encoder settings. For a controlled diagnosis of **desktop audio in obs**,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
