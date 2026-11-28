---
title: "OBS Capture Desktop Audio: Why the Meter Moves but the Recording Is Silent"
description: "Fix OBS capture desktop audio when the meter moves but the recorded file has no source audio. Step-by-step diagnosis for multi-track recordings."
seo_title: "OBS Capture Desktop Audio: Meter Moves but No Sound in Recording"
seo_description: "Fix OBS capture desktop audio when the meter moves but the recorded file has no source audio. Step-by-step diagnosis for multi-track recordings."
keywords:
  - "obs capture desktop audio"
date: 2026-11-28T22:13:16+08:00
publishDate: 2026-11-28T22:13:16+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

## Troubleshooting

You are recording a game and mic on separate tracks, and the desktop audio meter moves, but the recorded file has no source audio. Before you change anything, confirm the track routing in your recording output. Open Settings > Output, set Output Mode to Advanced, and select the Recording tab. Under Audio Track, note which track number is ticked. Then open Edit > Advanced Audio Properties. In the Tracks row for Desktop Audio, verify that the same track number is checked. If the meter moves but the track is unchecked, OBS captures the source but never writes it to the file. Check the result: the meter should still move while the track box is ticked. If it is unticked, tick it and close the dialog. Next, confirm the recording format. If you record to a format that does not support multiple tracks, OBS may flatten or drop tracks. Use MKV or MOV for multi-track recordings, then remux to MP4 if needed. Now run a verification test: record ten seconds with desktop audio playing, stop, and open the file in a player that shows track selection. Select the desktop audio track and confirm sound. If the track is present but silent, re-check the Advanced Audio Properties tick box. If you had changed the track assignment, roll back by restoring the previous track number and retest. For a guided check of your exact routing,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult). This keeps your **obs capture desktop audio** setup predictable without touching unrelated sources.

Repeat the same check after a restart and confirm the result twice.
