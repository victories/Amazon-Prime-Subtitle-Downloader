# Amazon Prime Subtitle Downloader

Amazon Prime Video'dan toplu altyazi indirmenizi saglayan bir userscript. Tum sezon veya tek film icin altyazilari SRT/TTML formatinda ZIP arsivi olarak indirebilirsiniz.

## Ozellikler

- Bir sezonun tum bolumlerinin altyazilarini tek seferde indirme
- Film altyazisi indirme
- Otomatik TTML -> SRT donusumu
- Birden fazla altyazi dili ve format destegi (SDH, forced narrative vb.)
- Dosya adinda bolum basligini ekleme (istege bagli)
- Ilerleme cubugu ve iptal destegi

## Kurulum

1. [Tampermonkey](https://www.tampermonkey.net/) veya [Violentmonkey](https://violentmonkey.github.io/) gibi bir userscript yoneticisi kurun
2. [Scripti yuklemek icin buraya tiklayin](https://raw.githubusercontent.com/victories/Amazon-Prime-Subtitle-Downloader/master/Amazon%20Video%20-%20subtitle%20downloader.user.js)

## Kullanim

1. Amazon Prime Video'da bir film veya dizi detay sayfasina gidin
2. Sayfanin tamamen yuklenmesini bekleyin (fragman otomatik oynatmasi altyazi verilerini tetikler)
3. Sayfanin ust-orta kismina fareyle gelerek "Amazon subtitle downloader" menusunu acin
4. Film veya tum sezon icin altyazilari indirmek icin tiklayin

## Desteklenen Siteler

- `*.primevideo.com`
- `*.amazon.com`
- `*.amazon.de`
- `*.amazon.co.uk`
- `*.amazon.co.jp`

## Krediler

Bu script, [Tithen-Firion](https://greasyfork.org/tr/users/100486-tithen-firion) tarafindan gelistirilen orijinal [Amazon Video - subtitle downloader](https://greasyfork.org/tr/scripts/34885-amazon-video-subtitle-downloader) scriptinin guncellemesidir.

### Orijinalden farklar (v3.0.0)

- Yeni Prime Video arayuzune (2025+) uyumlu hale getirildi
- Yeni `script[type="application/json"]` sayfa veri formati destegi eklendi (eski `script[type="text/template"]` yerine)
- Yeni `primaryActions[].payload.playback` yapisina gore aksiyon ayrıstirma guncellendi
- Yeni `/api/enrichItemMetadata` bolum yukleme API destegi eklendi
- `querySelector` yazim hatasi duzeltildi
- Degisken adi hatasi duzeltildi (`sub_name` -> `subName`)

---

# Amazon Prime Subtitle Downloader (English)

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
2. [Click here to install the script](https://raw.githubusercontent.com/victories/Amazon-Prime-Subtitle-Downloader/master/Amazon%20Video%20-%20subtitle%20downloader.user.js)

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
