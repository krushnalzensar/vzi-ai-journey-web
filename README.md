# VZI AI Journey

A single page telling VZI's story of becoming an AI powered enterprise: AI Commercial,
AI Safety and the VZI AI Lab. Built for Vedanta Zinc International, delivered with Zensar.

## What is in here

| File | What it is |
| --- | --- |
| `index.html` | The whole page. Fonts, styles, illustrations, logos and scripts are inside the file, so it fetches nothing from the internet at run time and also works offline. |
| `film.mp4` | The film, 8 minutes 3 seconds. |
| `demos/` | Four screen recordings from the build, opened by the Watch the demo buttons. |
| `vercel.json` | Long cache headers for the video files, no cache for the page. |

## Deploying

Any static host serves this as it stands: Vercel, Netlify, GitHub Pages, Azure Static
Web Apps, S3 with CloudFront, or an internal web server.

On Vercel, import the repository and keep the defaults:

- Framework preset: **Other**
- Root directory: **/** (the repository root)
- Build command: none
- Output directory: none

To preview or open it without a server, double click `index.html`. Chrome, Edge and
Safari all play the film from the file system.

## About the video files

Vercel refuses any single file over 100 MB, and a very large video is slow to start for
the viewer on any host. `film.mp4` is encoded from `VZI AI Journey Final v2.mp4` at the
same 1280 x 720 and the same frame rate, with the original audio track copied across
untouched. It measures 54.7 dB PSNR against the original, far above the level at which a
difference can be seen on screen, and it is 42 MB instead of 136 MB. Every mp4 here
starts with its index, so playback begins while the rest is still downloading.

If the exact original file is ever needed on the web, put it in object storage such as
Vercel Blob, Cloudflare R2 or S3 and point the `<video>` tag at that URL. The 100 MB
limit applies to files inside the deployment, not to media served from storage.

## Editing the page

`index.html` is generated, so changes are made in the source parts and the file is
rebuilt. Small wording fixes can be made directly in the file; anything structural is
better done in the source and rebuilt, otherwise the next build overwrites it.

## Credits

Vedanta Zinc International, with Zensar. 16 October 2026.
