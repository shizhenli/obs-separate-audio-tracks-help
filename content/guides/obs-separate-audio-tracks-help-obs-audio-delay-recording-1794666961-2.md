---
title: "OBS Audio Delay Recording: When the Meter Moves but the File Has No Source Audio"
description: "Troubleshoot OBS audio delay recording when the meter moves but the recorded file has no source audio. Check track assignments, sync offset, and verify with a short test recording."
seo_title: "OBS Audio Delay Recording: Fixing a Source That Shows Meters but Records Silence"
seo_description: "Troubleshoot OBS audio delay recording when the meter moves but the recorded file has no source audio. Check track assignments, sync offset, and verify with a short test recording."
keywords:
  - "obs audio delay recording"
date: 2026-11-23T12:02:37+08:00
publishDate: 2026-11-23T12:02:37+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording game and mic on separate tracks, and the meter moves but the saved file has no source audio, so you are stuck before a controlled diagnosis. This is often an **obs audio delay recording** issue where the source is live but routed or delayed out of the captured track.

## Check the source's track assignment

Open the source's properties and confirm the correct track is enabled. In the mixer, click the gear next to the source and verify the track checkboxes. If the source is only on a track that your recording output does not include, the meter still moves but the file stays silent. Result interpretation: if the source is unchecked on the track you expect, that is your cause.

## Check the sync offset

Right-click the source, open Filters, and inspect any Sync Offset filter. A large positive or negative offset can push audio outside the recorded segment, especially at the start. Set it to 0 ms temporarily. If the meter moves but the file has no audio, a nonzero offset is a strong suspect.

## Verify with a short test recording

Record 10 seconds while speaking and moving game audio. Stop, open the file in a player, and solo each track. If the source appears only after you remove the offset, the offset was the fault. If it is still missing, recheck the track checkboxes before changing anything else.

## Rollback and recovery

Before further edits, export your scene collection or note the original track and offset values. If a change makes things worse, restore those values and retest. For a guided diagnosis,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
