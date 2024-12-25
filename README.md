# Ethong

**Ethong** 是一個專為處理國台語夾雜語音的開源專案，目標是實現高效的語音辨識和翻譯。此專案基於 [Whisper](https://github.com/openai/whisper) 模型進行微調，並整合多語言翻譯模組，支援台羅文轉換與多語言翻譯（中文、英文、印尼文等）。專案同時提供即時語音處理 API，方便用於應用開發。

---

## **Features**
- **語音辨識**：支援國台語夾雜語音的高準確率辨識。
- **台羅文轉換**：將台語語音轉為台羅拼音文本。
- **多語言翻譯**：從台羅文翻譯成其他語言。
- **即時處理 API**：簡易整合至各類應用的即時語音處理服務。

---

## **Project Structure**
```
ethong/
├── notebooks/         # 用於數據探索與模型訓練的 Jupyter Notebooks
├── data/              # 存放語音數據與標註文件
├── models/            # 微調後的模型與相關檔案
├── ethong/            # 主代碼目錄
│   ├── __init__.py
│   ├── preprocess/    # 資料處理模組
│   ├── train/         # 模型訓練腳本
│   ├── translate/     # 翻譯功能模組
│   └── api/           # FastAPI 實作
├── tests/             # 測試代碼
├── pyproject.toml     # Poetry 配置文件
├── poetry.lock        # 所有依賴的具體版本
├── requirements.txt   # 相容性依賴列表
├── README.md          # 專案說明文件
└── .github/           # GitHub Actions 與 Issue 模板
```

---

## **Getting Started**

### **Environment Setup**
1. 安裝 [Poetry](https://python-poetry.org/):
   ```bash
   curl -sSL https://install.python-poetry.org | python3 -
   ```

2. 克隆專案:
   ```bash
   git clone https://github.com/yourusername/ethong.git
   cd ethong
   ```

3. 安裝依賴:
   ```bash
   poetry install
   ```

4. 如果需要 `requirements.txt` 支援:
   ```bash
   poetry export -f requirements.txt --output requirements.txt
   ```

### **Running the Project**
- **Notebook**: 在 `notebooks/` 中執行數據探索與測試。
- **微調模型**: 使用 `ethong/train/` 目錄下的腳本進行模型訓練。
- **啟動 API**:
  ```bash
  poetry run python ethong/api/main.py
  ```

---

## **Contributing**
歡迎提交 Issue 或 Pull Request！請確保所有代碼通過測試，並遵循代碼格式規範。

---

## **License**
[MIT License](LICENSE)
