# OurTube Channel Template

![Channel banner](assets/banner.png)

## What this is

This repository is a starter template for a channel on OurTube, an open-source YouTube-like site. It holds your channel details, a list of your videos, and a few images. You do not need to write any code.

When you finish the steps below, OurTube will find your channel automatically and show it on the site.

## Step 1: Create your repository

1. Tap **Use this template** at the top of this page.
2. Choose **Create a new repository**.
3. Give it a name and choose **Public**. Your channel must be public.
4. Tap **Create repository**.

## Step 2: Make it yours

Open `channel.json` and edit the name and description:

```json
{
  "name": "My Channel",
  "description": "Write a short description of your channel here.",
  "logo": "assets/logo.png",
  "banner": "assets/banner.png"
}
```

- `name` — your channel name.
- `description` — one or two sentences about your channel.

Then replace `assets/logo.png` with your own logo (square works best, 400x400) and `assets/banner.png` with your own banner (2048x512). Keep the same file names, or update the paths in `channel.json`.

## Step 3: Upload your video

Video files do not go inside this repository. Use GitHub Releases instead:

1. Go to the **Releases** tab of your repository.
2. Tap **Create a new release** (or **Draft a new release**).
3. Give it a tag, for example `v1`.
4. Drag your video file into the release (up to 2 GB per file).
5. Tap **Publish release**.
6. Open the uploaded file and copy its link. It looks like `https://github.com/you/repo/releases/download/v1/my-video.mp4`.

That link is your `videoUrl`.

## Step 4: Add the video to videos.json

Open `videos.json`. It is a list of videos. Add one object for each video or music track:

```json
{
  "id": "first-video",
  "title": "My First Video",
  "description": "What this video is about.",
  "thumbnail": "assets/first-video.jpg",
  "videoUrl": "https://example.com/my-video.mp4",
  "duration": "12:04",
  "type": "video",
  "tags": ["example"],
  "date": "2026-01-01"
}
```

- `id` — a short unique name with no spaces (used in the video link).
- `title` — the video title.
- `description` — a short description.
- `thumbnail` — a path to an image in `assets/`, or a full URL.
- `videoUrl` — the file link you copied in Step 3.
- `duration` — optional, shown on the thumbnail (for example `"12:04"`).
- `type` — `"video"` for videos, `"music"` for audio tracks.
- `tags` — a few words to help people find it.
- `date` — the publish date, for example `"2026-01-01"`.

Keep each `id` different, and put a comma between videos.

## Step 5: Add a thumbnail

1. Put your image in the `assets/` folder, for example `assets/my-video.jpg`.
2. Set that video's `"thumbnail"` to `"assets/my-video.jpg"`.

Use a 16:9 image, recommended size **1280x720**. You can also paste a full image URL instead.

## Step 6: Show up on OurTube

OurTube finds channels by a GitHub topic:

1. On your repository page, tap the **gear** icon next to **About**.
2. In **Topics**, add `openyoutube-channel`.
3. Save.

Your channel will now appear on OurTube.

## Tips

- The repository must be **Public**.
- `videos.json` must be **valid JSON** (watch the commas and quotes).
- **Never put video files inside the repository** — use Releases.
- Changes can take about **5 minutes** to appear on OurTube.
