# 阿莫迪兄妹談原則與信任：《The Builders》訪談導讀

Anthropic 共同創辦人 Dario Amodei 與 Daniela Amodei 在《The Builders》（Kaleidoscope）的訪談，全長 42:06，訪談錄於 2026-07-06，YouTube 影片 2026-10-27 上傳。這份導讀沿著主持人開場的問題「Anthropic 不做、對手會做的時候，他們退縮還是堅守原則」，把訪談中可對照的說法（Claude 憲法、不放廣告、五角大廈紅線、留任率、模型關機研究等）逐項對照官方文件，並標明哪些是講者自述、哪些已確認。

訪談全程沒有談 IPO；頻道說明提到 IPO，Anthropic 的 S-1 於影片上傳前一天公開，導讀只把它當時間背景。

## 製作聲明

本導讀的分析、撰稿、翻譯、查證、審稿與插圖由 AI 模型完成，**不是人類分析，也沒有經過人工逐句校稿**。

| 工作 | 模型／工具 |
|---|---|
| 主控、撰稿、字幕修詞、審稿統籌 | Claude Sonnet 5.5 |
| 審稿（事實、編輯、終審） | 全新對話的 Claude Sonnet subagent |
| 字幕逐句初譯 | Gemini 3.8 Flash（agy，medium 檔） |
| 長字幕完整讀取、音訊說話者輪替 | Gemini 4 Argon、Gemini 3.8 Flash（agy） |
| 總編輯潤稿、標示重點 | Claude Opus |
| 封面插畫（16:9、9:16、og 圖） | OpenAI Codex（imagegen） |
| 外部查證 | agy、OpenAI Codex、Claude Code 三路獨立，加上主控開啟官方頁面核對 |
| 音訊轉寫交叉比對 | 本機 Whisper（small.en） |

依據的是 YouTube 機器自動字幕（en-orig），沒有逐句對照原音；機器字幕與機器翻譯可能有誤。總編輯潤稿由 Claude Opus 依總編輯準則完成（只動語氣與重點標示，不動事實、引言與時間戳）。插圖只有封面一張，是 AI 生成的概念插畫，圖內沒有文字；時間線是頁面內建的 HTML 元件。

## 檔案

| 檔案 | 說明 |
|---|---|
| `index.html` | 導讀網頁（直接用瀏覽器開啟） |
| `amodei_siblings_builders_2026.md` | 導讀 Markdown 正文 |
| `translation-zh.html` | 全文繁中譯文（非官方，機器翻譯） |
| `player.html` | 雙語同步字幕播放器（需連網載入 YouTube；影片可內嵌） |
| `images/` | 封面插畫（`hero-16x9.webp`、`hero-9x16.webp`）與社群預覽圖 `og-hero.jpg` |
| `qa/` | 桌面 1440×900 與手機 390×844 截圖與 `qa_result.json` |
| `research/` | 需求、證據帳本、工作紀錄、逐句字幕與翻譯、審稿紀錄（只留本機，不公開） |

重建：`research/guide_src.md` 經 `python3 -I research/make_guide.py` 產生正文（同時檢查引言與時間戳），再依 `deep-guide-html` 的 `build_guide_html.py`、`build_player.py`、`cues_to_translation.py` 建置。

## 原始資料

- 影片：<https://www.youtube.com/watch?v=1OdoSzfUkec>（The Builders）
- 字幕：本機 `research/raw.srt`（來源為 `transcription/` 下同影片 id 的 SRT，`en-orig` 機器字幕，1107 個 cue，7797 字）；原始檔位置：`1_Product/exam31_notemaker/transcription/`。

## 重要來源

- Anthropic 官方：[Claude's new constitution](https://www.anthropic.com/news/claude-new-constitution)（2026-01-22）、[Claude is a space to think](https://www.anthropic.com/news/claude-is-a-space-to-think)（2026-02-04）、[Statement on the Department of War](https://www.anthropic.com/news/statement-department-of-war)（2026-02-26）、[S-1 公告](https://www.anthropic.com/news/s1-sec)（2026-10-26）、[A global workspace in language models](https://www.anthropic.com/research/global-workspace)（2026-07-06）。
- 國會文件：[S.4113](https://www.govinfo.gov/content/pkg/BILLS-119s4113is/html/BILLS-119s4113is.htm)、[S.4707](https://www.govinfo.gov/content/pkg/BILLS-119s4707is/html/BILLS-119s4707is.htm)。
- 第三方：[SignalFire 2025 報告](https://www.signalfire.com/blog/signalfire-state-of-talent-report-2025)。

完整來源見導讀文末〈來源清單〉。

## 狀態

**已發布（GitHub Pages）。**

- 正式網址：https://lushinshang.github.io/amodei_siblings_builders_2026/
- 發布日期：2026-10-29
- 發布內容：`index.html`、`player.html`、`translation-zh.html`、`amodei_siblings_builders_2026.md`、`README.md`、`images/`；`research/` 與 `qa/` 只留本機。

## 已知限制

- 說話者：字幕無說話者標記，只有問答脈絡可確認的段落歸給 Dario 或 Daniela，其餘寫「回答的創辦人」。
- 未驗證：OpenAI 官方協議頁（主控讀取回 403）、SEC S-1 全文（讀不到）、Anthropic 領導頁與國會文件以外的多數二手細節；真實 YouTube 嵌入播放（僅以假的 YT 物件測過）。
