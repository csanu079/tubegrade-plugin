# TubeGrade for Claude

![TubeGrade](assets/logo.png)

Find what's breaking out on YouTube, and why. This plugin connects Claude to
[TubeGrade](https://www.tubegrade.com/) and adds eight guided workflows for
YouTube creators: video ideas, planning your next upload, titles and
thumbnails, researched scripts, competitor breakdowns, video teardowns and
comment insights.

## What's inside

**One MCP connector.** The plugin adds TubeGrade's remote MCP server,
`https://api.tubegrade.com/mcp`. Its tools return public YouTube data: outlier
videos (videos that beat their own channel's normal views), viral title and
thumbnail formats, channel and video growth history, similar channels, weekly
channel rankings, transcripts, top comments, thumbnails as images, related
videos and autocomplete keywords. Two account tools keep a list of competitor
channels and saved videos in your TubeGrade account.

**Eight skills.** Each skill is a written workflow (a `SKILL.md` file plus
shared notes on what each tool returns). They tell Claude which tools to call,
how many calls to make, and what to deliver.

| Skill | What it does |
|---|---|
| `tubegrade-get-started` | What TubeGrade can do, checking your credit balance, and fixing common errors |
| `tubegrade-video-ideas` | Video ideas backed by videos that broke out in your niche |
| `tubegrade-next-video-planner` | Picks the single strongest next video for your channel |
| `tubegrade-packaging-studio` | Titles and thumbnail concepts from proven formats and real breakout thumbnails |
| `tubegrade-script-writer` | A researched script with timestamped citations from top videos' transcripts |
| `tubegrade-competitor-breakdown` | A rival channel's growth, breakout videos, packaging and hooks |
| `tubegrade-video-teardown` | Why one specific video worked or flopped |
| `tubegrade-comment-insights` | What viewers ask for and complain about, in their own words |

## Getting started

1. Install the plugin.
2. The first TubeGrade call asks you to sign in. Sign in with Google to your
   TubeGrade account, or create one in the same step.
3. Ask something like "Find videos that broke out in my niche this month and
   show me their thumbnails", or "Break down @channel's biggest recent
   outliers".

TubeGrade research calls draw on the credits in your TubeGrade account; each
tool's description states its cost before you use it, and account tools are
free. New accounts start with free credits.

## What this plugin runs and sends

- **No local code.** The plugin has no hooks, scripts, commands or local MCP
  servers. It is made of Markdown skills, two JSON configuration files and a
  logo.
- **One network destination.** Tool calls go only to
  `https://api.tubegrade.com/mcp`, over HTTPS. A call sends what that tool
  needs: a search query, a topic, or a YouTube channel or video id or URL.
  Saving a video or tracking a channel writes to your TubeGrade account.
- **Sign-in.** Authorization uses OAuth 2.1. The plugin never handles a
  password or token itself; Claude stores the connection.
- **No private YouTube data.** TubeGrade works from public YouTube data. It
  does not ask for or read your YouTube Analytics.

How TubeGrade handles data is described in its
[privacy policy](https://www.tubegrade.com/privacy/) and
[terms](https://www.tubegrade.com/terms/).

## Support

Help and contact: [tubegrade.com/support](https://www.tubegrade.com/support/)
or support@tubegrade.com.

## License

The skills and configuration in this repository are released under the MIT
License (see [LICENSE](LICENSE)). The TubeGrade service, its name and logo are
not covered by this license.
