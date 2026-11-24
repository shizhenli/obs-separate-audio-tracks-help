---
title: "OBS Audio Not Recording: When the Meter Moves but Your File Has No Source Audio"
description: "Fix OBS audio not recording when the meter moves but the recorded file has no source audio. Step-by-step checks for track routing, advanced audio properties, and a verification test."
seo_title: "OBS Audio Not Recording: Meter Moves but No Source Audio"
seo_description: "Fix OBS audio not recording when the meter moves but the recorded file has no source audio. Step-by-step checks for track routing, advanced audio properties, and a verification test."
keywords:
  - "obs audio not recording"
date: 2026-11-24T10:02:35+08:00
publishDate: 2026-11-24T10:02:35+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, the meter moves, but the file has no source audio. Let's diagnose this before changing anything else.

## Check the Track Assignment First

Open the mixer, click the gear next to the source, and choose Advanced Audio Properties. Look at the Track column for that source. If no track is checked, OBS meters the source but writes nothing to the recording. Enable Track 1 for the game and Track 2 for the mic, or match your intended layout. Then check Settings > Output > Recording. Confirm the recording format supports multiple tracks (MKV or MP4 with multiple audio tracks) and that the audio encoder is not set to a single track.

Interpretation: if a track box is empty, that is your cause. If boxes are checked, move on.

## Check the Recording Output Path

In Settings > Output > Recording, note the file path. Record ten seconds while speaking and playing game audio. Open the file in a player that lists audio tracks, such as VLC under Audio > Audio Track. If only one track appears, the multi-track setting did not apply. If tracks appear but are silent, the source is routed to a track that was not written.

## Verification Test

Create a fresh scene with only the mic. Record five seconds, then open the file and confirm the waveform. Repeat with only the game source. If each works alone but not together, the track layout is the fault. This is the controlled diagnosis for **obs audio not recording**.

## Rollback and Recovery

Before editing further, duplicate your scene collection (Scene Collection > Duplicate) so you can restore it. If a change makes things worse, switch back to the duplicate and reapply one setting at a time. Keep the original recording files untouched until you confirm the fix.

If the checks above do not isolate the track,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
