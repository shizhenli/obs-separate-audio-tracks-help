---
title: "OBS Capture Card Audio: When the Meter Moves but the Recording Is Silent"
description: "Fix OBS capture card audio that shows a moving meter but records no sound. Check track assignment, source sync, and run a verification test."
seo_title: "OBS Capture Card Audio Not Recording: Meter Moves but File Silent"
seo_description: "Fix OBS capture card audio that shows a moving meter but records no sound. Check track assignment, source sync, and run a verification test."
keywords:
  - "obs capture card audio"
date: 2026-11-28T21:45:29+08:00
publishDate: 2026-11-28T21:45:29+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and your capture card audio meter moves, but the recorded file has no source audio. This is a track-routing or source-state problem, not a capture card failure, so work through these checks before changing hardware.

## Check Track Assignment First

Open the Advanced Audio Properties window for your capture card source. Confirm the source is enabled on the track you expect. If the source is only checked on Track 1 while your recording settings write a different track, the meter will still move because monitoring is independent of track assignment. Interpretation: a moving meter with an unchecked target track means the source is live but not written. Enable the correct track and retest.

## Confirm the Source Is Not Muted or Filtered

Right-click the capture card source and inspect filters. A gain filter set very low, or a noise gate with an aggressive close threshold, can pass meter activity while attenuating the recorded signal. Temporarily bypass all filters and check the meter again. If the meter still moves but the file is silent, the issue is downstream in track or output settings, not the filter chain.

## Verify Output and Track Mapping

In Settings, Output, confirm the recording track selection matches the tracks you enabled. If you record multiple tracks, open the finished file in an editor that displays all tracks; many players only play Track 1. A file that seems silent may simply have your capture card on Track 2.

## Run a Verification Test

Record ten seconds with the capture card source active and speak into the mic. Stop, then open the file in a multitrack editor. Expected result: the capture card waveform appears on its assigned track. If it does not, revisit the track check above.

If the **obs capture card audio** still fails after these steps, keep a copy of your current scene collection before making further changes so you can roll back. For a guided diagnosis,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
