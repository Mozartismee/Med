# Gender Age Sampling

## 專案簡介
本專案的目的是從數據集中，依據性別和年齡進行隨機抽樣，以滿足指定的平均年齡和標準差條件。

該程式可用於醫療數據篩選、統計分析等應用場景，幫助用戶找到符合特定數據分佈條件的樣本。

## 主要功能
- 讀取 `df_cleaned` 數據集
- 按 `性別` 切分數據，確保抽樣人數符合條件
- 進行 10,000 次迭代隨機抽樣
- 計算抽樣後的平均年齡與標準差，篩選符合條件的結果
- 儲存符合條件的子集並輸出結果

## 環境需求
- Python 3.x
- Google Colab（推薦運行環境）
- 主要依賴庫：
  - `pandas`
  - `numpy`
  - `matplotlib`（可選，僅用於數據可視化）

## 使用方式
1. **下載專案**
   ```bash
   git clone https://github.com/your_username/Gender_Age_Sampling.git
   cd Gender_Age_Sampling
   ```
2. **在 Google Colab 中運行**
   - 將 `.ipynb` 文件上傳至 Google Colab。
   - 執行所有代碼區塊，確保 `df_cleaned` 數據已經準備好。
   
3. **運行 Python 腳本（本地環境）**
   若希望在本地執行 `.py` 版本，請確保安裝所有依賴：
   ```bash
   pip install pandas numpy
   ```
   然後運行程式：
   ```bash
   python gender_age_sampling.py
   ```

## 輸出範例
範例結果（來自 Google Colab 迭代 10,000 次後找到的最佳匹配）：
```
迭代次數: 9615
平均年齡: 63.91
標準差: 15.48
抽取的子集資料：
 年齡      病歷號 性別
 57 21891971  M
 38  2539479  M
 73  3460070  M
 ...
```

## 備註
- 若數據分佈與條件不符，可調整 `mean` 和 `std` 的範圍來增加匹配機率。
- 若運行時間過長，可減少 `iterations` 次數或增加 `範圍` 限制。

## 聯絡方式
如有任何問題，請聯絡 [your_email@example.com] 或在 GitHub issue 區回報問題。

