# Whisper Subtitle Generator | Whisper 字幕產生工具

**本工具使用 OpenAI 的 Whisper 模型，透過 Google Colab 實作，可將本地影片或 YouTube 影片自動轉換為逐字稿與 `.srt` 字幕檔。除了可手動上傳影片外，也整合 `yt-dlp` 套件，讓使用者僅需貼上 YouTube 連結即可自動下載影片並生成字幕。整體流程皆在雲端完成，無需在本機安裝任何環境設定，適用於影片紀錄、字幕生成、多語翻譯、無障礙輔助等場景。**
   
📑 詳細報告
更完整的技術原理、實作流程與結果討論，請參考：[WhisperAI_Report.pdf](WhisperAI_Report.pdf)

---

## 使用方式 (WhisperAI.ipynb)

1. 開啟 [Google Colab](https://colab.research.google.com)。  
2. 將 `WhisperAI.ipynb` 上傳或從 Google Drive 開啟。  
3. 將執行階段變更為 GPU（建議使用 T4 GPU）：  
   「執行階段」→「變更執行類型」→「硬體加速器」→ 選擇「GPU」。  
4. 依照 notebook 內的程式區塊與 Markdown 提示逐步執行。  
5. 所需 Python 套件已在 Colab 中自動安裝，無需額外設定。  
6. 上傳檔案即可進行語音辨識與字幕生成，最後下載 `.srt` 檔案應用於 YouTube 或其他平台。  

⚠️ 注意事項：  
- 使用時請登入 Google 帳戶，允許 Colab 存取 Drive（如需上傳/儲存檔案）。  
- 若遇資源限制，可稍後再執行，或嘗試不同區域的 Colab。  

---

## 📂 專案結構
```text
Whisper-Subtitle-Generator/
├── WhisperAI.ipynb          # Google Colab Notebook
├── README.md                # 專案說明
├── LICENSE                  # 授權條款
└── WhisperAI_Report.pdf     # 詳細技術報告

