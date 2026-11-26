---
title: "OBS Capture Audio Mac: Fixing a Source That Shows a Meter but Records No Audio"
description: "Fix OBS on Mac when the audio meter moves but the recorded file has no source audio. Check track assignments, macOS permissions, and run a quick verification test."
seo_title: "OBS Capture Audio Mac: Meter Moves but No Source Audio in Recording"
seo_description: "Fix OBS on Mac when the audio meter moves but the recorded file has no source audio. Check track assignments, macOS permissions, and run a quick verification test."
keywords:
  - "obs capture audio mac"
date: 2026-11-26T10:01:45+08:00
publishDate: 2026-11-26T10:01:45+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You're recording a game and mic on separate tracks in OBS on Mac, the meter moves, but the saved file has no source audio. Let's isolate the cause before changing anything else.

## Confirm the source is actually assigned to a track

Open the Advanced Audio Properties window (the gear icon in the Audio Mixer). Find the row for the source that shows activity. Under Tracks, make sure at least one track box is checked. A source can display a moving meter while being assigned to no track, which records silence. If no box is checked, check Track 1, then repeat for your mic. Click Close and save a short test recording.

## Check the track routing in Output settings

Go to Settings > Output. In Recording, confirm the recording format and that the audio track selection includes the tracks you enabled. If you're using a custom output mode, verify the track mapping hasn't been limited to a single track. Apply the change and record again.

## Verify macOS microphone permission

Open System Settings > Privacy & Security > Microphone. Confirm OBS is listed and enabled. If it isn't, toggle it on, then fully quit and reopen OBS. A permission change only takes effect after a restart.

## Run a verification test

Record ten seconds with the game audio and mic active. Stop, then open the file in a player that shows track selection, or import it into an editor and inspect each track. If the source audio appears on the expected track, the issue is resolved. If the meter still moves but the file is silent, revisit the track checkboxes first, since that is the most common cause of this exact symptom.

## Rollback note

If a recent change caused this, revert your last Output or Advanced Audio Properties edit before testing further. Keep a note of the original settings so you can restore them. For a guided diagnosis of your specific **obs capture audio mac** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
