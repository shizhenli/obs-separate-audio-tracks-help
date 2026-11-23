---
title: "OBS Audio Capture Card: Meter Moves but No Source Audio in Recording"
description: "Fix OBS audio capture card recordings where the meter moves but the file has no source audio. Check track assignment, monitoring, and run a quick verification test."
seo_title: "OBS Audio Capture Card Not Recorded: Fix Meter-Only Audio"
seo_description: "Fix OBS audio capture card recordings where the meter moves but the file has no source audio. Check track assignment, monitoring, and run a quick verification test."
keywords:
  - "obs audio capture card"
date: 2026-11-23T09:02:33+08:00
publishDate: 2026-11-23T09:02:33+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and your capture card's meter moves in OBS but the recorded file has no source audio.

## Confirm the source is actually assigned to a track

Open the Advanced Audio Properties window (the gear icon in the Audio Mixer). Find your capture card source and look at the track columns. A moving meter only proves the signal reaches OBS; it does not prove the source is routed to a recorded track. If none of the track boxes are checked for that source, or only a track you are not recording, the file will be silent. Check the box for the track you expect, then confirm that track is enabled under Settings > Output > Recording > Audio Track.

## Check monitoring and output routing

In the same window, verify the capture card is not set to Monitor Off in a way that misleads you. Monitoring affects what you hear, not what is written, but it helps you separate a routing problem from a device problem. Also confirm the correct device is selected in the source properties, not a duplicate or disabled input. If you recently changed the **obs audio capture card** settings, recheck the source properties for the active input.

## Run a verification test

Record 20 seconds while speaking or playing game audio. Stop, then open the file in a player and inspect each track. If the track now contains audio, the routing fix worked. If it is still silent, note which track is empty and recheck the Advanced Audio Properties boxes.

## Rollback note

If a recent change caused this, revert the track assignments and output settings to their previous values before retesting, so you do not stack fixes.

If the meter still moves but the file stays silent after these checks,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
