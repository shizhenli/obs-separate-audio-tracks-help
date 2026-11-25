---
title: "OBS Audio Recording Settings: When the Meter Moves but the File Has No Source Audio"
description: "Fix OBS recordings where the audio meter moves but the file has no source audio. Check track assignments, advanced settings, and verify with a short test recording."
seo_title: "OBS Audio Recording Settings: Meter Moves but No Source Audio"
seo_description: "Fix OBS recordings where the audio meter moves but the file has no source audio. Check track assignments, advanced settings, and verify with a short test recording."
keywords:
  - "obs audio recording settings"
date: 2026-11-25T09:02:34+08:00
publishDate: 2026-11-25T09:02:34+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and at the audio source is not captured step the meter moves but the recorded file has no source audio.

## Confirm the source is assigned to a recorded track

Open the mixer, click the gear next to the silent source, and choose Advanced Audio Properties. In the Tracks row for that source, note which boxes are checked. Then open Settings > Output > Recording and read the Track list. If the source is checked on Track 3 but only Track 1 is enabled for recording, the meter will still move while the file stays silent. Check the source on a track that the recording output actually writes, or enable that track in the output settings. Apply and close.

## Check the recording format and encoder

In Settings > Output > Recording, confirm the format. Some formats and encoders handle multiple tracks differently, and a mismatch can leave a source out of the saved file. If you recently changed the encoder, set it back to a known working option, then re-check the track boxes. This is where most **obs audio recording settings** problems hide, so change one value at a time.

## Run a verification test

Record ten seconds while speaking and triggering game sound. Stop, open the file in a player or editor that shows tracks, and inspect each track. Expected result: the mic appears on its assigned track and the game audio on its own track. If a track is empty, return to Advanced Audio Properties and confirm the box is checked for the track the file actually contains.

## Rollback if the test fails

Revert the last output or encoder change, restore the previous track layout, and record again before making further edits. If the source still does not appear,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your track layout and format details.
