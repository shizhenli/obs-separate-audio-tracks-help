---
title: "OBS Audio Capture Mac: When the Meter Moves but the Recording Has No Source Audio"
description: "Troubleshoot OBS audio capture on Mac when the meter moves but the recorded file has no source audio. Step-by-step checks, verification test, and rollback note."
seo_title: "OBS Audio Capture Mac: Fix Meter Moves, No Source Audio"
seo_description: "Troubleshoot OBS audio capture on Mac when the meter moves but the recorded file has no source audio. Step-by-step checks, verification test, and rollback note."
keywords:
  - "obs audio capture mac"
date: 2026-11-23T10:02:36+08:00
publishDate: 2026-11-23T10:02:36+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

## Troubleshooting

You are recording a game and mic on separate tracks in OBS on Mac, and you have reached the audio source is not captured step: the meter moves, but the recorded file has no source audio. Before changing anything, confirm the track matrix. Open Edit > Advanced Audio Properties and check that each source has a checkmark under the track you expect. If the game is on Track 1 and the mic on Track 2, both boxes must be ticked; a moving meter only proves the source is live, not that it is routed to a recorded track. Next, inspect Settings > Output. In Recording, confirm the output format and that the audio track selection includes the tracks you enabled. If you use a custom FFmpeg output, verify the mapping flags include every track; a missing map line drops that source silently. Then check Settings > Audio: the global sample rate must match your interface (typically 48 kHz), and the mic device must not be set to a different device than the one metering. Run a verification test: record ten seconds with the game and mic both active, stop, and open the file in QuickTime or Audacity. If the waveform shows only one channel or one track, return to Advanced Audio Properties and re-tick the missing track, then re-record. If the file is still silent, switch Recording Format to MKV, record again, and remux to MP4 via File > Remux Recordings; this preserves all tracks. Rollback note: if a recent change to output settings caused this, restore your previous profile via Profile > Manage Profiles before further edits. For a controlled diagnosis of your exact track layout,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult). This **obs audio capture mac** issue is almost always a routing checkbox or output mapping, not a dead source.
