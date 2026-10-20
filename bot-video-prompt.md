Make a 30-second motion graphics video about Grok Bot (https://x.ai/bot, https://x.com/bot), 1920×1080 at 60 fps, good enough to open a motion designer's showreel.

Research first

Read x.ai/bot and the u/bot profile. Use the product's real copy, the bot mark and the brand colors.

The site draws its bot icons from code, so rebuild the official shapes (circle, pebble, squircle, pill, triangle, hexagon, cloud, teardrop) from that geometry instead of redrawing them. Keep every bot flat 2D like the real mark: solid color, two pill eyes, no 3D shading.

Story (one idea at a time, each held long enough to read)

A stage light turns on, the Grok Bot drops in, wakes up and looks around. The camera pulls back to the lockup "Meet ◉ Grok Bot", with the bot itself sitting between the words.

It divides like a cell, 1 to 2 to 4 to 8, into colored bots, each with its own shape and job: "Give each Bot a job."

A glide into one bot's computer. It hops across tool tabs (Sheets, CRM, Research, Mail), signs in, does the work, and the finished email waits for your OK: "Signs in to your tools." / "Uses them like you do."

The screen switches off like an old TV. Night: "Your laptop sleeps." / "Your Bots don't." The bots pass work between them like a constellation while a clock runs through the night. Sunrise.

Daylight: the eight bots drop into a pile one by one, the Grok Bot lands last, then the wordmark, the tagline and x.ai/bot.

How to build it

No video models, no After Effects, no stock footage or audio. The only files you may use are fonts.

Write the renderer as a web page where every frame is a pure function of time: a WebGL2 shader for the bots (shape morphs, gooey merges, eyes projected on a sphere so they can look around, eyes kept inside the silhouette) and Canvas 2D for type and UI.

Render in headless Chrome with 8 or more jittered sub-frames per frame for motion blur, and pipe the frames into ffmpeg. Pull each frame out of Chrome in slices of 1 MB or less; one large DevTools message can hang without an error.

Lay the edit on a 128 BPM grid (64 beats = 30 s) so every scene change lands on a beat. Nothing moves too fast to follow: no whip pans, and every line of text stays up for at least a second.

Export a cue list from the timeline and synthesize the score and sound effects in Python from it, so every landing, pop and click hits its frame. Master to -14 LUFS.

You can't watch video or hear audio, so review with contact sheets of frames pulled from the actual encode, and check the mix by measuring loudness per octave. Fix what you find and render again.

Deliver the MP4, a copy under 30 MB for phones, a poster frame and a styleframes sheet.