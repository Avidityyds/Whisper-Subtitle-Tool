# Whisper Subtitle Generator | Whisper 字幕產生工具
 
**本工具使用 OpenAI 的 Whisper 模型，透過 Google Colab 實作，可將本地影片或 YouTube 影片自動轉換為逐字稿與多種格式字幕檔（TXT / SRT / VTT / JSON / TSV）。除了可手動上傳影片外，也整合 `yt-dlp` 套件，讓使用者僅需貼上 YouTube 連結即可自動下載影片並生成字幕。整體流程皆在雲端完成，無需在本機安裝任何環境設定，適用於影片紀錄、字幕生成、多語翻譯、無障礙輔助等場景。**
 
📑 詳細報告
更完整的技術原理、實作流程與結果討論，請參考：[WhisperAI_Report.pdf](WhisperAI_Report.pdf)
 
---
 
## ✨ 主要功能
 
| 類別 | 功能 |
|------|------|
| 影音來源 | YouTube URL 自動下載 ・ 本機上傳（mp3 / mp4 / m4a / wav / mov…）|
| 語言支援 | 中 / 英 / 日 / 韓 / 西 / 法 / 德 / 俄… **14+ 語言**，或自動偵測 |
| 辨識模型 | tiny → large-v3 共 6 種，自由切換準確度與速度 |
| 翻譯模式 | 將任意語言翻譯成英文（task = translate）|
| 輸出格式 | TXT ・ SRT ・ VTT ・ JSON ・ TSV（**五種格式**）|
| 進階設定 | Beam Size 調整 ・ 時間戳 ・ 低品質片段過濾 ・ Prompt 引導 |
| GPU 加速 | 自動偵測並使用 GPU |
| 雲端整合 | 自動同步輸出檔案至 Google Drive |
| 批次處理 | 支援多個 YouTube URL 一次辨識輸出 |
 
---
 
## 使用方式 (WhisperAI_Optimized.ipynb)
 
1. 開啟 [Google Colab](https://colab.research.google.com)。
2. 將 `WhisperAI_Optimized.ipynb` 上傳或從 Google Drive 開啟。
3. 將執行階段變更為 GPU（建議使用 T4 GPU）：  
   「執行階段」→「變更執行類型」→「硬體加速器」→ 選擇「GPU」。
4. 依序執行以下步驟：
   - **STEP 1**：安裝套件並檢查環境（GPU / Python / PyTorch 版本）
   - **STEP 2**：設定模型大小、語言、任務類型與進階選項
   - **STEP 3**：填入 YouTube URL 或上傳本機音影檔
   - **STEP 4**：載入模型並執行語音辨識
   - **STEP 5**：預覽辨識結果（全文 + 逐段時間軸 + 品質指標）
   - **STEP 6**：匯出並下載所需格式，或同步至 Google Drive
5. 所需 Python 套件已在 Colab 中自動安裝，無需額外設定。

⚠️ 注意事項：
- 使用時請登入 Google 帳戶，允許 Colab 存取 Drive（如需上傳 / 儲存檔案）。
- 若遇資源限制，可稍後再執行，或嘗試不同區域的 Colab。
---
 
## 📂 專案結構
 
```text
Whisper-Subtitle-Tool/
├── WhisperAI.ipynb  # Google Colab Notebook（舊版）
├── WhisperAI_Optimized.ipynb  # Google Colab Notebook（最新版）
├── README.md                  # 專案說明
├── LICENSE                    # 授權條款
└── WhisperAI_Report.pdf       # 詳細技術報告
```
 
