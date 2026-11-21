---
title: "Game Audio Capture OBS: When the Meter Moves but the Recording Is Silent"
description: "Troubleshoot game audio capture in OBS when the meter moves but the recorded file has no source audio. Step-by-step checks for track routing, advanced audio settings, and a verification test."
seo_title: "Game Audio Capture OBS: Fixing a Silent Track in Multi-Track Recordings"
seo_description: "Troubleshoot game audio capture in OBS when the meter moves but the recorded file has no source audio. Step-by-step checks for track routing, advanced audio settings, and a verification test."
keywords:
  - "game audio capture obs"
date: 2026-11-21T15:05:00+08:00
publishDate: 2026-11-21T15:05:00+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

**game audio capture obs**. You are recording a game and your mic on separate tracks, and OBS shows the game audio meter moving, yet the finished recording has no game audio. This is a track-routing problem, not a capture problem, and it is fixable with a few targeted checks.

## Confirm the source is actually assigned to a track

Open the Advanced Audio Properties window (the gear icon in the Audio Mixer). Find your game audio source and look at the Track columns. A moving meter only proves the source is receiving audio; it does not prove that audio is written to a track. If none of the Track 1–6 boxes are checked for that source, the meter will move while the file stays silent. Check Track 2 (or your chosen game track) and click Close. If the box was already checked, move to the next section.

## Check the recording track selection

In Settings > Output, under the Recording tab, confirm the recording format and that the track selection includes the track you assigned. If you record to a format that does not carry multiple tracks, such as some FLV configurations, switch to MKV or MP4 with multi-track support. Then verify in Settings > Audio that the sample rates for the game source and the recording match; a mismatch can drop the source from the file even when the meter responds.

## Run a verification test

Record 20 seconds of gameplay with the mic muted, then open the file in a player that exposes track selection, such as VLC under Audio > Audio Track. If the game track now plays, routing is fixed. If it is still silent, recheck the Track boxes and the output track selection together.

## Rollback note

If a change makes things worse, restore your previous Advanced Audio Properties and Output settings before continuing, so you always have a known working baseline.

For a guided diagnosis of your exact setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
