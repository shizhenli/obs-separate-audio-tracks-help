---
title: "No Audio in OBS Recording: When the Meter Moves but the File Is Silent"
description: "Fix OBS recordings where the meter moves but the file has no source audio. Step-by-step checks for track routing, source assignment, and a verification test."
seo_title: "No Audio in OBS Recording: Meter Moves, File Silent? Fix It"
seo_description: "Fix OBS recordings where the meter moves but the file has no source audio. Step-by-step checks for track routing, source assignment, and a verification test."
keywords:
  - "no audio in obs recording"
date: 2026-11-22T08:02:39+08:00
publishDate: 2026-11-22T08:02:39+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording game and mic on separate tracks, the meter moves, but the saved file has no source audio. This is a track-routing problem, not a capture problem.

## Check Track Assignment

Open the Advanced Audio Properties for your audio sources. Confirm each source has a checkmark under the track you intend to record. A moving meter only proves OBS receives audio; it does not prove the source is assigned to a recorded track. If the source is checked only on a track you are not recording, the file will be silent for that source. Set the game to Track 1 and the mic to Track 2, or whatever your plan requires, then apply.

## Check Output Track Selection

In Settings, Output, Recording, confirm the recording format supports multiple tracks and that the track list includes the tracks you assigned. If you record to a format that flattens tracks, verify the mix includes your sources. Also confirm you are not recording only a track that has no sources assigned.

## Verification Test

Record ten seconds while speaking and triggering game sound. Stop, then open the file in a player that shows track selection. Switch between tracks. Each track should carry its assigned source. If one track is silent, return to Advanced Audio Properties and recheck that source's track assignment.

## Rollback Note

If you changed track assignments and the result is worse, restore your previous Advanced Audio Properties settings and output track list before retesting. Keep a note of the working configuration.

If the meter still moves while the file stays silent after these checks, this is the point where a controlled diagnosis of your exact track layout is faster than more guessing.

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your source list and track assignments. This addresses **no audio in obs recording** at the routing stage, before you re-record.
