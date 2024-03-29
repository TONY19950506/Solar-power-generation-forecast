# AIdea 太陽能發電量預測競賽

本項目參與了 AIdea 平台上由 ITRI 和 Surplux Energy 聯合舉辦的太陽能發電量預測競賽。該競賽旨在透過機器學習方法，基於歷史太陽能發電資料（如日照量、裝置容量等）預測未來太陽能發電量，以促進再生能源的發展和利用。

## 競賽概要

- **目標**：利用機器學習預測各地太陽能發電量，找出影響發電量的關鍵因素。
- **獲獎標準**：在 Private Leaderboard 上的 RMSE 分數低於 260。
- **時間範圍**：2022 年 4 月 20 日至 2022 年 7 月 6 日。

## 競賽成果

- **參與次數**：共計 18 次提交。
- **最終排名**：
  - Public Leaderboard：第 22 名 / 179。
  - Private Leaderboard：第 30 名 / 179。

## 資料說明

競賽提供以下數據集，供參賽者訓練和測試模型：

- **訓練資料集** (`train.csv`)：包含 3,785 筆數據。
- **測試資料集** (`test.csv`)：包含 1,350 筆數據。

每條記錄包含以下欄位：資料編號（ID）、資料日期（Date）、緯度（Lat）、經度（Lon）、模組型號（Module）、裝置容量（Capacity）、預測目標-發電量（Generation）、當日平均氣溫（Temp）、模溫計-模板溫度（Temp_m）、日射量（Irradiance）、日照計-日射量（Irradiance_m）等。

## 解決方案摘要

- **異常值處理**：基於陣列轉換率，定義並移除異常值。
- **缺失值處理**：對缺失值進行補值或刪除處理，以提高數據質量。
- **特徵工程**：選擇和轉換特徵，提升模型的預測能力。
- **模型訓練**：使用 XGBoost 等機器學習算法進行訓練和預測。
- **超參數調優**：透過 Hyperopt 對模型進行超參數調優，優化預測性能。

