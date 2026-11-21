---
title: "Capture Computer Audio OBS: When the Meter Moves but the Recording Is Silent"
description: "Fix OBS recording silence when the meter moves but the file has no source audio. Step-by-step checks for track routing, advanced audio settings, and verification."
seo_title: "Capture Computer Audio OBS: Meter Moves but No Source Audio"
seo_description: "Fix OBS recording silence when the meter moves but the file has no source audio. Step-by-step checks for track routing, advanced audio settings, and verification."
keywords:
  - "capture computer audio obs"
date: 2026-11-21T15:01:46+08:00
publishDate: 2026-11-21T15:01:46+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You're recording game and mic on separate tracks, the meter bounces, but the saved file has no source audio. That points to a routing or track assignment issue, not a dead source. Here's how to isolate it.

## Check the source's track assignment
Open the Advanced Audio Properties window (gear icon in the Audio Mixer). Find your game capture source. Under Tracks, confirm the track you intend to record is checked. If only Track 1 is checked but your recording settings expect Track 2, the meter will move while the file stays silent. Check the track you actually want, then click Close.

## Confirm output track selection
Go to Settings > Output. In Recording, ensure the audio track checkboxes match the tracks you assigned. If you record Track 1 only but the source is on Track 2, you'll get silence. Enable the correct track here as well.

## Verify the source isn't muted downstream
In the mixer, confirm the source isn't muted and its fader is up. Also check any filters (e.g., a gain filter set to -inf). A moving meter with silence often means the signal is routed to a track that isn't being written.

## Run a verification test
Record 10 seconds of known audio (game sound plus speech). Stop, then open the file in a player that shows channels or use OBS's remux to inspect tracks. If the source appears on the expected track, routing is fixed. If not, revisit the track checkboxes.

## Rollback note
If you changed multiple settings, revert to your last working profile via Profile > Duplicate before testing again, so you can compare behavior cleanly.

If the meter still moves but the file lacks source audio after these checks, the issue may be a corrupt profile or conflicting plugin. For a guided diagnosis of your **capture computer audio obs** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
