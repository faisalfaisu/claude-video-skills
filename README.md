# Claude Video Skills

From **AI with Faisal** on YouTube.

Type a prompt in Claude Code and get a finished video: explainers, reels, whiteboard, paper cutout, pixel art, anime, 3D and motion design. Every video is built with code (HyperFrames + GSAP) and rendered to MP4 on your own computer.

## How it works

1. **You type a prompt**, for example `/whiteboard explain where good ideas come from`.
2. **A skill** (a folder with a `SKILL.md`) tells Claude exactly how to build that kind of video.
3. **HyperFrames** turns the HTML and animation code Claude writes into frames.
4. **FFmpeg** encodes the frames into `video.mp4`.

The first try is close, not perfect. Look at it and ask Claude for fixes: "make the title bigger", "slow down scene 2", "add a whoosh on every cut".

## What you need

| | What | Why |
|---|---|---|
| 1 | **Claude Code** on a paid Claude plan (Pro or Max) | Runs the skills. The desktop app's Code tab or the Terminal both work. |
| 2 | **Node.js 22 or newer** | Runs HyperFrames. Download from nodejs.org. |
| 3 | **FFmpeg** | Makes the MP4. Mac: `npm i -g ffmpeg-static`. Windows: `winget install ffmpeg` in PowerShell. |
| 4 | **Python 3.9+ with Pillow and NumPy** | Image and audio helpers. Mac: `pip3 install pillow numpy`. Windows: install Python from python.org (tick "Add python.exe to PATH"), then `python -m pip install pillow numpy`. |
| 5 | **Windows only: Git for Windows** | Claude Code needs it on Windows. git-scm.com |

## Install the skills (about 10 minutes, one time)

1. Download this folder (the ZIP link from the comment) and unzip it.
2. Pick one way:
   - **Double-click** `1. Install (Mac).command` or `1. Install (Windows).bat`. On Mac, if it is blocked the first time: right-click it, then Open, then Open.
   - **Or let Claude do it:** open Claude Code and type `install the skills from this folder:` and drag this folder into the chat.
   - **Or by hand:** copy every folder inside `skills` into `~/.claude/skills` (Mac) or `C:\Users\<you>\.claude\skills` (Windows).
3. **Check it works:** double-click `2. Self-test (Mac).command` or `2. Self-test (Windows).bat`. It renders a 3-second test video. "ALL PASSED" means you are ready.
4. **Close and reopen Claude Code.**

If you already had skills with the same names, the installer saves your old copies in `.claude/skills-backup` first.

## Start making videos

Type one of these in Claude Code:

| Skill | What it makes | Try |
|---|---|---|
| `/edit` | **Start here.** Picks the right skill for you, storyboards, builds, adds sound, checks the result | `/edit make a 20 second launch video for my app "Flowly", 9:16` |
| `/director` | The full editing pipeline with 11 looks (Creator Explainer, SaaS, Vox, Bold Impact and more) | `/director turn this script into a Vox-style explainer` |
| `/reels` | 9:16 Reels / TikTok / Shorts from your own talking-head clip | `/edit edit ~/Downloads/myclip.mp4 as a reel` |
| `/youtube` | 16:9 YouTube edits with key words, zooms and side cards | `/youtube edit interview.mp4 with a lower third and chapter titles` |
| `/saas` | Product and app promos built from a prompt, no footage needed | `/saas a 20 second promo for a habit tracker app` |
| `/whiteboard` | A hand draws your idea live, marker by marker | `/whiteboard explain where good ideas come from` |
| `/paper-cutout` | Cut-paper characters on layered paper scenes | `/paper-cutout a cat shares apples with a friend` |
| `/pixel-art` | A retro game world, pixel by pixel | `/pixel-art a kid flies a kite at sunset` |
| `/anime-cel` | Anime frames, reactions and close-ups | `/anime-cel she gives him a letter, big close-up` |
| `/crayon-storybook` | A children's picture book in crayon | `/crayon-storybook a bear who can't sleep` |
| `/painted-animation` | Watercolour-and-ink cartoon | `/painted-animation a fox walks through autumn rain` |
| `/vox-director` | Vox-style documentary with collage and archive looks | `/vox-director a 60 second story of how money began, 9:16` |
| `/faceless-explainer` | Explainer from any text, no footage | `/faceless-explainer turn this article into a 30 second Short` |
| `/threejs-animation` | 3D scenes and characters | `/threejs-animation a 15 second 3D stick-figure story on a metro` |
| `/particle-system`, `/shader-glsl` | Particles, glow, shader backgrounds | `/particle-system a confetti burst for my end card` |
| `/video-clone` | Copies the look of a reference video in your own content | `/video-clone make a video like this one about my topic: <link>` |
| `/music-to-video` | Visuals cut to a song's beat | `/music-to-video lyric video for song.mp3` |
| `/embedded-captions` | Captions on a talking-head video, even behind you | `/embedded-captions add captions to talk.mp4` |
| `/sound` | Sound effects on the exact frame and a -14 LUFS mix | `/sound add SFX and music to video.mp4` |
| `/qa` | Checks format, loudness, sync and every frame before you post | `/qa check video.mp4` |

The `skills` folder has more (camera moves, transitions, motion rules, Figma import, FFmpeg and others). Each one explains itself in its own `SKILL.md`.

## Tips

- Say the length and the format in your prompt: "20 seconds, 9:16".
- Ask for a storyboard first, then say "build it".
- Use your own music or the code-made sound from `/sound`, so your video is safe to post.
- Rendering runs on your computer and can take a few minutes for a 30-second video.

## Licences

Each skill keeps its original open-source licence. See `LICENSE`, `CREDITS.md` and the `licenses` folder.
