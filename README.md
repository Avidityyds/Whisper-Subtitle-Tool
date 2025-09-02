# 🎧 Whisper Subtitle Generator | Whisper 字幕產生工具

**本工具使用 OpenAI 的 Whisper 模型，透過 Google Colab 實作，可將本地影片或 YouTube 影片自動轉換為逐字稿與 `.srt` 字幕檔。除了可手動上傳影片外，也整合 `yt-dlp` 套件，讓使用者僅需貼上 YouTube 連結即可自動下載影片並生成字幕。整體流程皆在雲端完成，無需在本機安裝任何環境設定，適用於影片紀錄、字幕生成、多語翻譯、無障礙輔助等場景。

**This project uses OpenAI's Whisper model via Google Colab to automatically convert local or YouTube videos into transcripts and `.srt` subtitle files. In addition to manual file uploads, the tool also integrates the `yt-dlp` package, allowing users to paste a YouTube link and automatically download and transcribe the video. The entire workflow runs in the cloud without requiring any local setup, making it ideal for content creators, educators, language learners, and accessibility support.

---
### WhisperAI.ipynb 使用說明


本專案所提供的 WhisperAI.ipynb 為一份使用 Google Colab 平台進行實作的jupyter notebook檔案。結合 Whisper 開源模型，能夠將上傳的影片或音訊檔案轉換為文字並輸出字幕檔（.srt），可應用於影片字幕製作、語音資料整理等場景。

使用方式如下：
1. 開啟 Google Colab（ https://colab.research.google.com ）。
2. 將 WhisperAI.ipynb 上傳或從 Google Drive 開啟。
3. 請先將執行階段變更為 GPU（建議使用 T4 GPU）：  
   點選「執行階段」→「變更執行類型」→「硬體加速器」選擇「GPU」。
4. 依照 jupyter notebook 中的程式區塊順序與 Markdown 提示逐步執行。
5. 所需的 Python 套件與依賴項已在 Colab 中自動安裝與設定，無需在本機額外安裝任何軟體。
6. 上傳檔案後即可進行語音辨識與字幕生成，最終可下載 .srt 檔案應用於其他平台（例如 YouTube）。

注意事項：
- 使用時請確認已登入 Google 帳戶，並允許 Colab 存取您的 Drive（如有需要上傳／儲存檔案）。
- 若遇到資源限制，可稍待一段時間再重新啟動執行階段。

如有進一步問題，請參考筆記本中的說明註解或 Markdown 區塊內容。
