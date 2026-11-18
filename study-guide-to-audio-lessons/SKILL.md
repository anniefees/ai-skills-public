---
name: study-guide-to-audio-lessons
description: >-
  Use this to turn a written study guide into detailed audio lessons with free local text to speech.
status: draft
updated: 2026-11-17
---
# Study guide to audio lessons

## Steps
1. Pull the full study guide, including any nested or linked sections, and apply any sourced corrections.
2. Write a spoken script that covers everything: chapters by topic, abbreviations spelled out, no symbols, key numbers repeated, memory tricks, and 3 to 5 pause-and-answer questions at the end of each chapter.
3. Generate one MP3 per chapter with a free local text to speech tool (for example edge-tts), then join them with ffmpeg.
4. Check every file with ffprobe and a full decode. Rebuild stalled chapters in parts.
5. If your chat app caps attachments (for example 25 MB), re-encode as mono 32 kbps 22 kHz. Send the full file first, then the chapters.
6. Save the script with the audio.

## Rules
- Cover everything; don't summarize.
