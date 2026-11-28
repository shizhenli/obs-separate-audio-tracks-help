---
title: "OBS Capture Computer Audio: When the Meter Moves but the Recording Has No Source Audio"
description: "Fix OBS capture computer audio when the meter moves but the recorded file has no source audio. Check track assignments, advanced audio settings, and run a verification test."
seo_title: "OBS Capture Computer Audio: Meter Moves but No Source Audio in Recording"
seo_description: "Fix OBS capture computer audio when the meter moves but the recorded file has no source audio. Check track assignments, advanced audio settings, and run a verification test."
keywords:
  - "obs capture computer audio"
date: 2026-11-28T21:45:29+08:00
publishDate: 2026-11-28T21:45:29+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording game and mic on separate tracks, and at the audio source is not captured step you see the meter move but the recorded file has no source audio. Let's diagnose this in a controlled way before changing anything else.

## Check Track Assignments First

Open the Advanced Audio Properties for your audio sources. For the game or desktop source, confirm at least one track box is checked under Tracks. If the meter moves but no track is assigned, OBS monitors the signal but does not write it to the file. Assign the source to Track 1 or a dedicated track and note which track you expect it on. Repeat for the mic source so each has its own track.

## Confirm Output Track Mapping

In Settings, Output, Recording, verify the audio track count matches your assignments. If you record to a format like MP4, check that the container includes all tracks. A mismatch here can leave a source out of the file even when the meter moves.

## Run a Verification Test

Record ten seconds with the game audio and mic both active. Stop, then inspect the file in a player that shows track selection, or open it in an editor. If the game source appears on the assigned track, the fix held. If it is still silent, return to Advanced Audio Properties and confirm the checkboxes saved after closing the dialog.

## Rollback Note

If you changed multiple settings, revert to your previous track layout and reapply one change at a time. This keeps the working mic track intact while you isolate the missing source. For a guided review of your **obs capture computer audio** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
