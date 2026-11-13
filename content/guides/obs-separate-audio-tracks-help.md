---
title: 'OBS Multi-Track Recording Only Has Track 1: What to Check'
description: Trace OBS audio from source to track to output file, then verify every stream in a player.
seo_title: OBS Only Records One Audio Track? Check Routing
seo_description: Trace OBS audio from source to track to output file, then verify every stream in a player.
keywords:
- obs only one audio track
- obs separate audio tracks missing
- obs multi track recording
date: '2026-11-13'
draft: false
categories:
- Video Recording
category_slug: video-recording
---

<p>OBS can display several audio tracks while writing only one. The fix is to prove each source's track assignment and inspect the resulting file outside OBS.</p>
<h2>Before you start</h2><ul>
<li>OBS version and the scene collection</li>
<li>One microphone and one desktop audio source</li>
<li>A short recording folder</li>
<li>A player or editor that lists audio streams</li>
</ul>
<h2>Step-by-step checks</h2>
<h3>Step 1: Map sources to tracks</h3>
<p>Open Advanced Audio Properties and write down the track numbers for mic, desktop, and any game source. Keep track 1 as a safety mix only if you need it.</p>
<p><strong>Check:</strong> Every intended source has a unique track number.</p>
<h3>Step 2: Enable tracks in output</h3>
<p>In Settings → Output → Recording, confirm the audio track selection includes all mapped tracks. Check the recording format supports multiple audio streams.</p>
<p><strong>Check:</strong> The output track checkboxes match the mapping.</p>
<h3>Step 3: Record a labeled test</h3>
<p>Say “microphone track” into the mic while playing a short desktop sound. Record 20 seconds, stop, and note the exact output path.</p>
<p><strong>Check:</strong> The recording is long enough to hear both sources.</p>
<h3>Step 4: Inspect streams outside OBS</h3>
<p>Open the file in a player or editor that lists audio streams. Solo each track and confirm the expected source; a waveform on one track only is a failure.</p>
<p><strong>Check:</strong> Each intended track has the correct audio and no unintended mix.</p>
<h3>Step 5: Save and repeat once</h3>
<p>Save the profile/scene collection, restart OBS, and record a second short test. The same tracks should appear without remapping.</p>
<p><strong>Check:</strong> The second file has the same verified track layout.</p>
<h2>Verify the result</h2>
<p>The test file has separate, audible tracks for each intended source, and the saved profile reproduces them after an OBS restart.</p>
<h2>Rollback</h2>
<p>Keep the previous profile/scene collection export. Restore it if the new routing causes a source to disappear.</p>
<p><a href="/#consult">Ask for help with this exact symptom</a> · <a href="/guides/">All troubleshooting guides</a></p>
