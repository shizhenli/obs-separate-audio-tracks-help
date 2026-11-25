---
title: "OBS Audio Settings for Recording: When the Meter Moves but the File Is Silent"
description: "Fix OBS recordings where the audio meter moves but the recorded file has no source audio. Check track assignments, advanced audio settings, and run a verification test."
seo_title: "OBS Audio Settings for Recording: Meter Moves, File Silent"
seo_description: "Fix OBS recordings where the audio meter moves but the recorded file has no source audio. Check track assignments, advanced audio settings, and run a verification test."
keywords:
  - "obs audio settings for recording"
date: 2026-11-25T10:02:32+08:00
publishDate: 2026-11-25T10:02:32+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

## Troubleshooting

You are recording a game and mic on separate tracks, the meter moves, but the recorded file has no source audio. This points to a track routing problem, not a dead source. Before changing anything, open Edit > Advanced Audio Properties and confirm each source's track checkboxes. The meter proves the source is live; the checkboxes decide where it lands in the file. If the game is checked only on Track 2 and your recording output is set to Track 1, the file will be silent for that source even though the meter moves. Check that every source you need has at least one track enabled and that Settings > Output > Recording has the matching tracks selected. A common trap: Track 1 is checked globally but the source itself is not assigned to Track 1. Fix the assignment, not the volume. Next, verify with a short ten-second test recording: speak, move in-game, stop, then open the file in a player that shows track selection. If the mic appears on Track 2 and the game on Track 3, routing is correct. If a track is empty, return to Advanced Audio Properties and re-check that source. If you changed multiple **obs audio settings for recording** at once and the result worsened, roll back by restoring your previous output track selection and re-testing one change at a time. Keep a note of the original checkbox state so recovery is quick. If the meter still moves and the file stays silent after these checks, stop guessing and get a controlled diagnosis:

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).
