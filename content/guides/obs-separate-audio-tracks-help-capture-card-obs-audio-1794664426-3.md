---
title: "Capture Card OBS Audio: Meter Moves but No Source Audio in Recording"
description: "Fix capture card OBS audio when the meter moves but the recording has no source audio. Check track assignment, monitoring, and advanced audio settings."
seo_title: "Capture Card OBS Audio Not Recorded: Meter Moves but File Silent"
seo_description: "Fix capture card OBS audio when the meter moves but the recording has no source audio. Check track assignment, monitoring, and advanced audio settings."
keywords:
  - "capture card obs audio"
date: 2026-11-21T15:01:46+08:00
publishDate: 2026-11-21T15:01:46+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You're recording gameplay and mic on separate tracks in OBS, and your capture card's meter moves, but the recorded file has no source audio. Let's diagnose this step by step.

## Check Track Assignment

Open the Advanced Audio Properties for your capture card source (gear icon > Advanced Audio Properties). Under Tracks, ensure the track you intend to record is checked. If only Track 1 is checked but your recording output uses Track 2, the meter will move while the file stays silent. Verify your Output settings (Settings > Output > Recording) match the track you've enabled.

## Check Monitoring and Device

In the same Advanced Audio Properties window, set Monitoring to "Monitor Off" unless you need to hear it. More importantly, confirm the correct device is selected in the source properties. A common trap: the meter shows activity from a different input than the one being recorded. Click the source, open Properties, and reselect your capture card's audio device explicitly.

## Run a Verification Test

Create a short 10-second recording with a known sound (e.g., game menu music). After stopping, play the file in a media player and watch the track meters. If the meter moves but you hear nothing, the track is present but muted or routed incorrectly. If no meter moves, the track wasn't recorded at all—return to track assignment.

## Rollback and Recovery

If you changed multiple settings, revert to your last working scene collection (Scene Collection > Duplicate, then test). Keep a backup of your OBS profile before further edits.

If the **capture card obs audio** still won't record after these checks,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your OBS logs and a sample file.
