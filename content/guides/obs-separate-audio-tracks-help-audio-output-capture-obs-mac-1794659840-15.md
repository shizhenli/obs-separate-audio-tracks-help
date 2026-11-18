---
title: "Audio Output Capture OBS Mac: Meter Moves but Recording Has No Source Audio"
description: "Fix OBS on Mac when the audio meter moves but the recorded file has no source audio. Step-by-step checks for audio output capture, track routing, and a verification test."
seo_title: "Audio Output Capture OBS Mac: Fix Meter Moves, No Audio in Recording"
seo_description: "Fix OBS on Mac when the audio meter moves but the recorded file has no source audio. Step-by-step checks for audio output capture, track routing, and a verification test."
keywords:
  - "audio output capture obs mac"
date: 2026-11-18T10:10:40+08:00
publishDate: 2026-11-18T10:10:40+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks in OBS on Mac, and the meter moves, but the recorded file has no source audio.

## Check the source's track assignment
Open the Advanced Audio Properties window (the gear icon in the Audio Mixer). For the source whose meter moves, confirm at least one track checkbox is enabled. If the source is assigned only to Track 2 but your recording output only writes Track 1, the file will be silent for that source. Enable the track that matches your recording output, then re-test.

## Confirm the recording output tracks
In Settings > Output > Recording, check the audio track selection. If you record to a single track, every source must be assigned to that track. If you use multiple tracks, note which track each source uses. A mismatch here is the most common cause of a moving meter with silence in the file.

## Verify with a short test recording
Record 10 seconds while speaking and playing game audio. Stop, then open the file in a player that shows track selection, or import it into an editor and inspect each track. If the source's track is empty, return to Advanced Audio Properties and correct the assignment. If the track contains audio, the issue is in your player or export step, not OBS.

## Rollback note
If you changed track assignments and the recording worsens, reopen Advanced Audio Properties and restore the previous checkboxes. Keep a note of the original layout before editing.

For a controlled diagnosis of your **audio output capture obs mac** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
