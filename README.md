# Trend Desk

A daily rundown of trending clips from TikTok, Instagram, YouTube and X, written up as podcast segments.

- `index.html`: the site. It reads `data/dates.json` and `data/YYYY-MM-DD.json`, and embeds each clip with the platform's official player.
- `data/YYYY-MM-DD.json`: one file per day, written by the scheduled task.

## Day file format

```json
{
  "date": "2026-11-26",
  "generated_at": "2026-11-26T12:05:00Z",
  "note": "optional one-liner about the day",
  "segments": [
    {
      "title": "Segment headline",
      "category": "Funny / viral | News | Pop culture | Tech & gaming",
      "why_trending": "1–2 sentences: what it is and why it's popping now",
      "talking_points": ["...", "..."],
      "host_questions": ["...", "..."],
      "angle": "optional suggested take or debate framing",
      "clips": [
        {"platform": "TikTok", "url": "https://www.tiktok.com/@user/video/123", "title": "...", "creator": "@user", "views_note": "~4.2M views"}
      ]
    }
  ]
}
```
