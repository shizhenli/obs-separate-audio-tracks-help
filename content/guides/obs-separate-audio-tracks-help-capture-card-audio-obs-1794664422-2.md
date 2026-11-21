---
title: "Capture Card Audio in OBS: Meter Moves but No Source Audio in Recording"
description: "Fix capture card audio in OBS when the meter moves but the recording has no source audio. Step-by-step checks for track assignment, source sync, and verification."
seo_title: "Capture Card Audio OBS: Fix Meter Moves but No Recorded Audio"
seo_description: "Fix capture card audio in OBS when the meter moves but the recording has no source audio. Step-by-step checks for track assignment, source sync, and verification."
keywords:
  - "capture card audio obs"
date: 2026-11-21T14:58:41+08:00
publishDate: 2026-11-21T14:58:41+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You're recording gameplay and mic on separate tracks, but when you play back the file, the capture card's meter moved during recording yet the source audio is missing. That points to a track routing issue, not a dead capture card.

## Check Track Assignment on the Capture Card Source

Open the Advanced Audio Properties for your capture card source. Confirm the source is assigned to the track you expect (for example, Track 2 for game audio). If it's only on Track 1 and you're recording Track 2 alone, the meter will still move because OBS monitors the source, but the file won't contain it. Result interpretation: if the source has no checkmark on your recording track, that's your cause. Enable the correct track and close the dialog.

## Confirm the Recording Track Is Enabled

In Settings > Output > Recording, check the Audio Track(s) field. It must include the track you assigned. If it lists only Track 1, your capture card track is excluded. Add the correct track number, then apply.

## Verify with a Short Test Recording

Record 15 seconds while the capture card meter is active. Stop, open the file in a player that shows track selection, and confirm the capture card audio is present on the expected track. If it is, the routing is fixed. If not, recheck the source's Advanced Audio Properties for a muted or disabled track.

## Rollback Note

If you changed multiple audio settings, revert to your previous track layout before retesting so you can isolate which change mattered. Keep a note of the original track numbers.

If the meter still moves without recorded audio after these checks, the issue may be in the capture card's own audio output settings or OBS source properties.

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your OBS log and a sample recording for a controlled diagnosis of your **capture card audio obs** setup.
