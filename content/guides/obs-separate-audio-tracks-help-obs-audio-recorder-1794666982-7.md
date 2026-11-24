---
title: "OBS Audio Recorder: When the Meter Moves but the File Has No Source Audio"
description: "Fix OBS audio recorder when the meter moves but the recorded file has no source audio. Check track assignments, source routing, and verify with a short test recording."
seo_title: "OBS Audio Recorder: Meter Moves but No Source Audio in Recording"
seo_description: "Fix OBS audio recorder when the meter moves but the recorded file has no source audio. Check track assignments, source routing, and verify with a short test recording."
keywords:
  - "obs audio recorder"
date: 2026-11-24T12:03:32+08:00
publishDate: 2026-11-24T12:03:32+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

## Troubleshooting

You are recording a game and mic on separate tracks in OBS Studio, and at the audio source is not captured step the meter moves but the saved file has no source audio. Start by opening Edit > Advanced Audio Properties and confirm the source's Track checkboxes. The meter shows the source is live, but a track must be enabled for that source or it will not be written to the file. If the source has no track checked, enable the track you intend to record and apply the change. Next, check Settings > Output. In recording mode, confirm the audio track selection includes the track you just enabled. A common cause is recording only Track 1 while the source is assigned to Track 2. Set the recorder to include both tracks, or move the source to the recorded track, then apply. Also verify the source is not routed only to a monitor device: in Advanced Audio Properties, set Audio Monitoring to Monitor Off unless you need monitoring, since monitoring does not affect the recording but can mask routing mistakes. Run a verification test: record 15 seconds with the game audio and mic active, stop, and open the file in a player that shows track selection. Confirm each track contains the expected source. If a track is still silent, note which track is empty and recheck that source's checkbox. If you changed multiple settings, roll back by restoring the previous track assignments and output track selection before retesting one change at a time. For a controlled diagnosis of your **obs audio recorder** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
