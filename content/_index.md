---
title: OBS Separate Audio Tracks Help
seo_title: OBS Separate Audio Tracks Help | Only Track 1 Fix
seo_description: Remote OBS help for multi-track recordings that only contain track 1, with source routing and player verification.
keywords:
- obs only one audio track
- obs separate audio tracks missing
- obs multi track recording
hero_kicker: OBS MULTI-TRACK RECORDING
hero_h1: OBS recorded only one audio track?
hero_lead: Record a short test, inspect every track in the output file, and confirm the intended microphone and desktop sources before editing.
hero_proof:
- One short test recording
- Every track checked in a player
- Source-to-track mapping documented
hero_alt: A streaming desk with a microphone and OBS multi-track recording panel
hero_title: OBS multi-track audio recording setup
body_alt: An OBS audio mixer showing separate microphone and desktop tracks
body_title: OBS audio track routing check
body_caption: A track exists only when it is assigned, recorded, and readable in the exported file.
failures_kicker: THE THREE FAILURES WE SEE
failures_heading: What is going wrong?
test_kicker: HOW WE TEST
test_heading: Find the failing layer, then prove the fix.
scope_kicker: SERVICE SCOPE
scope_heading: What is included
scope_note: The session covers one agreed device and one verified path. Anything outside the written scope is quoted separately before work starts.
faq_kicker: FAQ
faq_heading: Before you book
consult_heading: Tell us what is happening.
consult_lead: Send the device, software, exact symptom, and what you have already tried. We will confirm scope and a fixed quote before booking.
form_placeholder: Device, software version, exact symptom, and what you have tried.
first_guide_url: /guides/obs-separate-audio-tracks-help/
symptoms:
- title: The file has one track
  text: A recording that should contain mic and desktop audio plays only the first track in a video editor.
- title: A source is silent
  text: The meter moves in OBS, but the intended track is empty after export.
- title: The editor cannot see tracks
  text: The player or editor shows a single mixed stream even though OBS displays several tracks.
checks:
- title: Assign each source to a track
  text: Open Advanced Audio Properties and record which source is on which track. Do not assume the mixer order is the file order.
- title: Record a 20-second test
  text: Capture mic and desktop audio on separate tracks, then stop and locate the actual output file.
- title: Inspect the file outside OBS
  text: Use a media player or editor that displays audio streams. Confirm each intended track has audio and the correct source.
- title: Save the working profile
  text: Export or document the OBS profile and scene collection so the routing can be repeated.
included:
- One OBS scene and one short test recording
- Source-to-track mapping
- Track inspection in a player/editor
- Profile and rollback notes
excluded:
- Editing a full production
- Repairing corrupted recordings
- Buying audio hardware
- Guaranteeing every editor supports the container
faqs:
- q: Why does OBS show six tracks but the file has one?
  a: Tracks must be assigned in Advanced Audio Properties and enabled in the recording output. A track can exist in the UI without being written.
- q: Which format should I use?
  a: Use a recording format your editor reads and that supports multiple audio streams. Test the exact container before a long session.
- q: Can you recover a already-recorded file?
  a: We can inspect it, but a missing stream usually cannot be reconstructed. The safe path is to fix routing and record a new test.
---
