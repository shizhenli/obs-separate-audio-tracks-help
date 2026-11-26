---
title: "OBS Capture Audio from Window: Meter Moves but Recording Has No Source Audio"
description: "Fix OBS window capture audio that shows a moving meter but records silence. Step-by-step checks for track routing, monitoring, and source settings."
seo_title: "OBS Capture Audio from Window: Fix Meter but No Recorded Audio"
seo_description: "Fix OBS window capture audio that shows a moving meter but records silence. Step-by-step checks for track routing, monitoring, and source settings."
keywords:
  - "obs capture audio from window"
date: 2026-11-26T09:01:45+08:00
publishDate: 2026-11-26T09:01:45+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and at the audio source is not captured step the meter moves but the recorded file has no source audio. Start by confirming which source is silent in the file. Play the recording and note whether the mic track works while the window capture track is empty. If only the window source is missing, the meter is likely showing monitoring activity rather than recorded output.

## Check the source's track assignment

Open the source properties for your window capture and verify that at least one track is checked under Tracks. If no track is selected, the meter still moves but nothing is written. Select the intended track, click OK, and record a short test. A correct result is a file where that track contains audio; if the track stays empty, continue below.

## Check monitoring and output routing

In Advanced Audio Properties, confirm the window source is set to Monitor Off or Monitor and Output, not Monitor Only. Monitor Only feeds your speakers but excludes the source from the recording. Also confirm the source is not muted and its volume is above zero. Record ten seconds and inspect the file again.

## Verification test

Create a fresh scene with only the window capture and one track enabled. Record a short clip while the window plays sound. Open the file in a player that shows track selection and confirm the track has a waveform. If it does, the original scene had a routing conflict; re-enable tracks one at a time to find it. If it does not, the window may be outputting to a device OBS is not capturing, so set OBS to capture that device directly.

## Rollback and recovery

Before changing more settings, export your scene collection so you can restore it. If a test makes things worse, re-import the export and return to the last working configuration. For a guided diagnosis of your **obs capture audio from window** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
