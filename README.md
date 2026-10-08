# Miteiru: Designing an Open-Source Subtitle-Immersion Player for Japanese, Mandarin, Cantonese and Vietnamese, Before and With AI Coding Assistants

Hocky Yudhiono, Independent researcher, Hong Kong SAR

**PDF:** see the [latest release](https://github.com/hockyy/miteiru-paper/releases/latest). The software itself is [hockyy/miteiru](https://github.com/hockyy/miteiru).

Miteiru is an open-source desktop video player for learning Japanese, Mandarin, Cantonese and Vietnamese from the subtitles of real video. This paper describes its design and architecture, gives the rationale for twelve design decisions traced to the commits and issues where they were made, argues that Cantonese needs a language mode of its own rather than a Mandarin setting, and compares the project's 32 months written without AI coding assistants with the 12 months written with them.

## Contents

| Path | What |
|---|---|
| `main.tex`, `refs.bib`, `main.bbl` | The paper (pdfLaTeX-compatible; plain ASCII) |
| `figures/` | Figures as included by `main.tex` |
| `figures/src/` | XeLaTeX sources of the two CJK figures (`fig_tokens`, `fig_cantonese`) |
| `data/` | Every measurement behind the paper; see [`data/README.md`](data/README.md) |
| `abstract.txt` | The abstract as plain text |

## Building

Built with [Tectonic](https://tectonic-typesetting.github.io/) 0.17; pdfLaTeX gives the same layout.

```bash
tectonic main.tex --keep-intermediates
```

The two CJK figures are compiled separately with XeLaTeX and need the Windows fonts Yu Gothic, Microsoft YaHei, Microsoft JhengHei and Segoe UI (JhengHei covers the Hong Kong characters). Their `Path=` option assumes this folder sits two levels below the drive root (for example `C:\Users\<name>\miteiru-paper`); adjust it elsewhere.

```bash
cd figures/src
tectonic --outdir .. fig_tokens.tex
tectonic --outdir .. fig_cantonese.tex
```

## Screenshots and video sources

Figures 1, 2 and 5 show frames and subtitles from four public YouTube videos whose uploaders subtitled their own speech; they are credited in the paper's Appendix A. The frames are shown for research commentary and are not covered by any licence of this repository.
