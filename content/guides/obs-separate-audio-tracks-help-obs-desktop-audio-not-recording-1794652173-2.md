---
title: "OBS Desktop Audio Not Recording: When the Meter Moves but the File Is Silent"
description: "Fix OBS desktop audio not recording when the meter moves but your recorded file has no source audio. Step-by-step checks, a verification test, and rollback note."
seo_title: "OBS Desktop Audio Not Recording: Meter Moves, File Silent"
seo_description: "Fix OBS desktop audio not recording when the meter moves but your recorded file has no source audio. Step-by-step checks, a verification test, and rollback note."
keywords:
  - "obs desktop audio not recording"
date: 2026-11-15T18:46:08+08:00
publishDate: 2026-11-15T18:46:08+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and the desktop audio meter moves, but the finished file has no source audio. This is a track-routing problem, not a capture problem.

## Confirm the source is actually assigned to a track

Open the Audio Mixer, click the gear next to Desktop Audio, and choose Advanced Audio Properties. In the Tracks row for that source, note which boxes are checked. If only Track 1 is checked but your recording output uses Track 2, the meter will still move while the file stays silent. Check at least one track that your recording settings actually write to.

## Check the recording output track selection

Go to Settings, Output, and switch the output mode to Advanced. Under the Recording tab, inspect the Track checkboxes. The tracks enabled here must overlap with the tracks assigned to Desktop Audio. A mismatch is the usual cause of **obs desktop audio not recording** even when levels look healthy.

## Verify with a short controlled test

Record ten seconds with desktop audio playing and your mic muted. Stop, open the file in a player that shows audio channels, and confirm the desktop track contains sound. If it does, the routing is fixed. If it does not, recheck the track boxes before changing anything else.

## Rollback note

Before editing Advanced Audio Properties, screenshot your current track assignments. If the test fails, restore those exact checkboxes so you return to a known state rather than stacking changes.

If the mismatch persists after these checks,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your track assignments and output settings.
