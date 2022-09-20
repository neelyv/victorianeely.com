---
layout: post
title: "My File Naming and Editing System for LibriVox Recordings"
date: 2022-07-02 00:00:00
category: LibriVox
tag: LibriVox
---

# My File Naming and Editing System for LibriVox Recordings

When recording audiobook chapters for LibriVox, I have a system for naming and working on the audio files I've recorded in Audacity.

When I first do my recording, I name the first AUP file something like this:

`booktitle_section#_authorlastname_128kb-raw.aup`

I replace `booktitle` with the title of the work, `section#` with the chapter or section number (e.g, `02` for chapter two), and `authorlastname` with the last name of the author. The word `raw` indicates a recording I haven't touched or edited in any way. I keep the raw version as a backup in case I make a mistake in the working file.

When I'm ready to start editing my recording, I save a copy of the original file with a new name:

`booktitle_section#_authorlastname_128kb-working.aup`

The `working` part indicates that this is the AUP file I'm editing. This is where I trim long pauses, re-record bad sections, and basically clean things up.

When I'm happy with the recording and ready to run some final effects to polish it up, I save a new copy of the edited file:

`booktitle_section#_authorlastname_128kb-polished.aup`

I apply the final effects to this `polished` file, such as amplifying or de-amplifying, compressing, normalizing, etc. I do these steps in a separate file in case a LibriVox proof listener finds mistakes and asks me to redo parts of my recording.

Finally I convert the `polished` AUP file to an MP3 file. I rename the MP3 to fit LibriVox's naming conventions and then upload it for proof listening.

**Note:** If a proof listener asks me to make changes to the recording, I go back to my `working` file to make my fixes and proceed from there. This helps ensure that any newly recorded sections fit seamlessly with the rest.

