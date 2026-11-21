---
title: "Best Audio Settings for OBS Recording: When the Meter Moves but the File Has No Source Audio"
description: "Fix OBS recordings where the meter moves but the file has no source audio. Check track assignments, encoder settings, and run a verification test."
seo_title: "Best Audio Settings for OBS Recording: Fix Meter Moves but No Audio"
seo_description: "Fix OBS recordings where the meter moves but the file has no source audio. Check track assignments, encoder settings, and run a verification test."
keywords:
  - "best audio settings for obs recording"
date: 2026-11-21T14:58:41+08:00
publishDate: 2026-11-21T14:58:41+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording game and mic on separate tracks, and at the audio source is not captured step the meter moves but the recorded file has no source audio. Here is a controlled way to isolate the cause.

## Check Track Assignments First

Open the Advanced Audio Properties for each source. Confirm the game and mic each have at least one track enabled, and that those tracks are not both set to the same number. If a source has no track checked, OBS shows a live meter but writes nothing for that source. Result interpretation: if a source has zero tracks enabled, that is your cause. Enable the intended track and recheck.

## Confirm the Recording Output Mode

In Settings, Output, Recording, verify the recording format and encoder. If you use a custom ffmpeg output, track mapping can silently drop sources. Switch temporarily to a standard recording format and the default encoder. This is also where you confirm the **best audio settings for obs recording**: 48 kHz sample rate, stereo, and one track per source.

## Run a Verification Test

Record ten seconds while speaking and playing game audio. Stop, then open the file in a player that shows track selection. If the file has multiple tracks, switch between them. If only one track exists and it is silent, return to Advanced Audio Properties and recheck every source. If the correct track now contains audio, the fix is confirmed.

## Rollback and Recovery

Before changing encoder or format, duplicate your current profile so you can restore it. If the test fails after changes, reload the saved profile and change only one setting at a time. If the meter still moves but the file stays silent,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your OBS log and a short test recording.
