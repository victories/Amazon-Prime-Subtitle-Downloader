# Amazon Prime Subtitle Downloader

A userscript that allows you to download subtitles from Amazon Prime Video in bulk. Supports downloading subtitles for entire seasons or individual movies as SRT/TTML files packed in a ZIP archive.

## Features

- Download subtitles for all episodes of a season at once
- Download subtitles for individual movies
- Automatic TTML to SRT conversion
- Supports multiple subtitle languages and formats (SDH, forced narratives, etc.)
- Episode title in filename (optional)
- Progress bar with cancel support

## Installation

1. Install a userscript manager like [Tampermonkey](https://www.tampermonkey.net/) or [Violentmonkey](https://violentmonkey.github.io/)
2. [Click here to install the script](https://raw.githubusercontent.com/victories/Amazon-Prime-Subtitle-Downloader/main/Amazon%20Video%20-%20subtitle%20downloader.user.js)

## Usage

1. Navigate to a movie or TV show detail page on Amazon Prime Video
2. Wait for the page to fully load (the trailer autoplay triggers subtitle data loading)
3. Hover over the top-center of the page to reveal the "Amazon subtitle downloader" menu
4. Click to download subtitles for the movie or the entire season batch

## Supported Sites

- `*.primevideo.com`
- `*.amazon.com`
- `*.amazon.de`
- `*.amazon.co.uk`
- `*.amazon.co.jp`

## Credits

This is a fork of the original [Amazon Video - subtitle downloader](https://greasyfork.org/tr/scripts/34885-amazon-video-subtitle-downloader) by [Tithen-Firion](https://greasyfork.org/tr/users/100486-tithen-firion).

### Changes from the original (v3.0.0)

- Updated to work with the new Prime Video UI (2025+)
- Added support for the new `script[type="application/json"]` page data format (replaces old `script[type="text/template"]`)
- Updated action parsing for new `primaryActions[].payload.playback` structure
- Added support for the new `/api/enrichItemMetadata` episode loading API
- Fixed typo in `querySelector` call
- Fixed variable name bug (`sub_name` -> `subName`)

## License

MIT
