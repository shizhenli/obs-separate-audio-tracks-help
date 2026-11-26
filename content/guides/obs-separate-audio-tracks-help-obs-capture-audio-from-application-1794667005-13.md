---
title: "OBS Capture Audio from Application: Meter Moves but Recording Has No Source Audio"
description: "Fix OBS capture audio from application when the meter moves but the recorded file has no source audio. Step-by-step checks for track routing, monitoring, and encoder settings."
seo_title: "OBS Capture Audio from Application: Meter Moves but No Source Audio"
seo_description: "Fix OBS capture audio from application when the meter moves but the recorded file has no source audio. Step-by-step checks for track routing, monitoring, and encoder settings."
keywords:
  - "obs capture audio from application"
date: 2026-11-26T08:01:49+08:00
publishDate: 2026-11-26T08:01:49+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and OBS shows the application meter moving, but the saved file plays back with no source audio. That points to a routing or track-assignment problem, not a dead source. Here is a controlled diagnosis.

## Check the source's track assignment

Open the Advanced Audio Properties window for the application source. Confirm the source is assigned to at least one track that is actually being recorded. A moving meter only proves the source is receiving audio; it does not prove that audio is written to a track. If the source sits on a track that is not enabled in Settings > Output > Recording, the file will be silent for that source.

## Check the encoder track selection

In Settings > Output, verify which tracks the recording encoder includes. If only track 1 is enabled and your application source is on track 2, the meter will move while the file stays silent. Enable the track that carries the source, or move the source to an enabled track.

## Check monitoring and output routing

Make sure the source is not set to Monitor Off in a way that misleads you, and confirm the correct output device is selected. A meter can move from monitoring while the recording path remains disconnected.

## Verification test

Record a short 20-second clip with the application playing. Stop, open the file in a player that shows track selection, and confirm the source track contains audio. If it does not, recheck the track assignment before changing anything else.

## Rollback note

If a recent change caused this, revert the last audio or output setting and retest. Keep a note of the working track layout so you can restore it quickly.

If the meter still moves while the file stays silent, this is the point to get a second set of eyes on your exact layout:

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult). For a reliable fix to **obs capture audio from application**, confirm the source track is enabled in the encoder before touching anything else.
