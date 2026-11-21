---
title: "Best OBS Audio Settings for Recording: When the Meter Moves but the File Has No Source Audio"
description: "Fix OBS recordings where the meter moves but the file has no source audio. Check track assignments, advanced audio settings, and run a quick verification test."
seo_title: "Best OBS Audio Settings for Recording: Fix Meter Moves but No Audio"
seo_description: "Fix OBS recordings where the meter moves but the file has no source audio. Check track assignments, advanced audio settings, and run a quick verification test."
keywords:
  - "best obs audio settings for recording"
date: 2026-11-21T14:58:41+08:00
publishDate: 2026-11-21T14:58:41+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording game and mic on separate tracks, but the meter moves while the saved file has no source audio. This points to a track routing issue, not a dead source. Before changing anything, note your current Audio settings so you can roll back.

## Check Track Assignments

Open Settings > Output, set Output Mode to Advanced, and select the Recording tab. Under Audio Track, confirm at least one track is selected. Then open Edit > Advanced Audio Properties. For each source (game and mic), verify the Track 1, Track 2, etc. boxes match the tracks you enabled in Output. If a source has no track box checked, OBS meters it but writes nothing. Check the box for the intended track.

## Check Encoder and Container

In Settings > Output > Recording, confirm the encoder supports multiple audio tracks (for example, FFmpeg with a container like MKV or MP4). If you use a simple mode or a container that drops extra tracks, switch to MKV, which preserves separate tracks. This is often the missing piece when tuning the **best obs audio settings for recording**.

## Verification Test

Record 15 seconds with game audio and mic both active. Stop, then open the file in a player that shows audio tracks (VLC: Audio > Audio Track). Confirm each track plays the expected source. If one track is silent, return to Advanced Audio Properties and recheck that source's track box.

## Rollback Note

If the test fails, revert the track checkboxes and encoder/container changes to your previous values, then re-record. Keep a screenshot of your original settings to restore quickly. If the source still will not capture after these checks,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your Output and Advanced Audio Properties screenshots.
