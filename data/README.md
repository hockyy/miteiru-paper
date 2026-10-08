# Data behind the paper

Everything here was measured on 8–9 October 2026 against Miteiru 7.5.2 (`main` at `41c6eb3`).

- `commits.csv`: one row per commit on the first-parent history of `main` (633 rows): date, author, subject, subject length, message-body lines, co-author trailers, files and lines changed. "code" columns count only TypeScript, JavaScript, Python, C#, Objective-C and CSS; all columns exclude `package-lock.json`, `renderer/public/`, JSON data, images and `app/`.
- `history_monthly.csv`: commits per month and source lines at the end of each month (Figure 7).
- `analyzer/`: the input lines (`*.txt`) and Miteiru's token output (`*.json`) from its local analyzer server, used for Figures 4 and 6. `timings.csv` is the whole-file tokenization timing of Section 5.4 (five runs per language); the subtitle files themselves are the video creators' text and are not included.
- `cantonese_subtitle_register.csv`: the subtitle-register screen (Table 2). For each video: the subtitle track used, the count of written-Cantonese markers and of Standard Written Chinese markers.

## The register markers

Written Cantonese (26 characters): 嘅 咗 佢 喺 冇 啲 唔 嘢 睇 嚟 咩 乜 噉 咁 啱 搵 畀 俾 嗰 哋 㗎 喎 囉 嘞 吖 咪

Standard Written Chinese (15 forms): 的 了 他 她 在 沒有 没有 些 不 這 这 們 们 什麼 什么

The score is the Cantonese share of all marker hits in a track. The screen used five YouTube searches with the "has subtitles" filter (廣東話 vlog 香港; 粵語 字幕 香港 日常; 香港 youtuber 廣東話字幕; 廣東話 煮飯; 香港 街訪), took the videos with an uploader-made track in a Chinese language code (`zh`, `zh-HK`, `zh-Hant`, `zh-TW`, `yue-HK`), and scored those under 30 minutes. The spoken language of each video was not verified.

