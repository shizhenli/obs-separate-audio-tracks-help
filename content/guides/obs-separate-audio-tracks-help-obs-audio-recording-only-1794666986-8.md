---
title: "OBS Audio Recording Only: When the Meter Moves but the File Has No Source Audio"
description: "Fix OBS recording where the audio meter moves but the saved file has no source audio. Check track assignments, advanced output settings, and verify with a short test recording."
seo_title: "OBS Audio Recording Only: Meter Moves but No Source Audio in File"
seo_description: "Fix OBS recording where the audio meter moves but the saved file has no source audio. Check track assignments, advanced output settings, and verify with a short test recording."
keywords:
  - "obs audio recording only"
date: 2026-11-25T08:02:39+08:00
publishDate: 2026-11-25T08:02:39+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

## Troubleshooting

You are recording game and mic on separate tracks in OBS Studio, the meter moves, but the recorded file contains no source audio. This is an **obs audio recording only** failure where the source is not captured despite visible activity. Start by confirming the source is actually assigned to a recorded track. Open the Advanced Audio Properties window and check the Track columns next to your game and mic sources. A moving meter only proves the source is live; it does not prove it is routed to a track. If the boxes are unchecked, the file will be silent even though the meter moves. Next, open Settings, then Output, and confirm the recording format and track count. In Advanced output mode, verify that the audio track bitrate is not zero and that the track you expect is enabled. In Simple mode, check that the recording audio track is set to the track containing your sources. If the track count is one but your sources are on track two, the file will have no source audio. Run a verification test: record ten seconds while speaking and playing game audio, then open the file in a media player and inspect the audio channels. If the meter moved but the file is silent, the track routing is still wrong. If the file now has audio, the fix is confirmed. Before changing more settings, export your current profile so you can roll back if a later adjustment breaks another recording. If the problem persists after checking track assignments and output settings,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your OBS log and a short sample recording.
