---
title: "OBS Best Audio Settings for Recording: When the Meter Moves but the File Has No Source Audio"
description: "Fix OBS recordings where the meter moves but the file has no source audio. Check track assignments, advanced audio settings, and run a verification test."
seo_title: "OBS Best Audio Settings for Recording: Fix Meter Moves But No Audio"
seo_description: "Fix OBS recordings where the meter moves but the file has no source audio. Check track assignments, advanced audio settings, and run a verification test."
keywords:
  - "obs best audio settings for recording"
date: 2026-11-25T11:02:36+08:00
publishDate: 2026-11-25T11:02:36+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording gameplay and mic on separate tracks in OBS, but at the audio source is not captured step the meter moves while the recorded file contains no source audio. Here is a controlled diagnosis to restore the expected outcome.

## Check Track Assignments in Advanced Audio Properties

Open Edit > Advanced Audio Properties. For each source (game and mic), confirm the correct track is checked under Tracks. A common cause is a source being assigned only to Track 2 while the recording output is set to Track 1. If the meter moves but the file is silent, the source is likely routed to a track that is not being written. Verify that each source has at least one track enabled that matches your recording output. Also confirm that no source is accidentally muted at the track level.

## Confirm Output Track Selection

Go to Settings > Output > Recording. Under the Recording tab, check the Audio Track setting. If it is set to Track 1, only sources assigned to Track 1 will be recorded. For separate tracks, ensure the container supports multiple audio tracks (e.g., MKV or MP4) and that the track selection includes the tracks your sources use. If you need a starting point, these are the **obs best audio settings for recording**: assign each source to its own track and set the output to record all tracks.

## Verification Test

Record a 10-second clip with both sources active. Play it back in a media player that shows track selection, or import it into an editor and inspect each audio track. If the meter moved during recording but a track is silent, the source is not assigned to that track. If all tracks are silent, check the source's volume and mute state.

## Rollback and Recovery

Before changing settings, export your current profile via Profile > Export. If the fix does not work, re-import the profile to restore your previous configuration. If you need guided help,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
