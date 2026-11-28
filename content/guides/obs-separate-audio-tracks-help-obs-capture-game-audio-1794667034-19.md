---
title: "OBS Capture Game Audio: Meter Moves but Recording Has No Source Audio"
description: "Fix OBS capture game audio when the meter moves but the recorded file has no source audio. Check track assignments, advanced audio settings, and verify with a short test recording."
seo_title: "OBS Capture Game Audio: Meter Moves but File Is Silent"
seo_description: "Fix OBS capture game audio when the meter moves but the recorded file has no source audio. Check track assignments, advanced audio settings, and verify with a short test recording."
keywords:
  - "obs capture game audio"
date: 2026-11-28T22:13:16+08:00
publishDate: 2026-11-28T22:13:16+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

## Troubleshooting

You are recording a game and mic on separate tracks, and at the audio source is not captured step the meter moves but the saved file has no source audio. Start by opening Edit > Advanced Audio Properties. For your game capture source, confirm the track boxes match the tracks you actually record in Settings > Output > Recording. A common miss: the meter shows activity, but the source is only checked on Track 2 while the recording output is set to Track 1. Set the game source to Track 1 and the mic to Track 2, or enable both tracks in the recording output. Next, check the source's volume and sync offset; a muted source or an extreme negative offset can make the meter look active while the audio lands outside the recorded range. Also confirm the correct audio device is selected in the source properties, not a disconnected default. Now run a verification test: record 15 seconds of gameplay with the mic muted, stop, and open the file in a player that shows track selection. If Track 1 now contains game audio, the track mapping was the cause. If it is still silent, right-click the game source, open Filters, and remove any gain or noise gate filter temporarily, then repeat the test. Before changing more settings, export your current profile so you can roll back. If the file remains silent after these checks, restore the exported profile and

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your OBS log and a sample recording. This keeps your **obs capture game audio** diagnosis controlled instead of guessing at random settings.
