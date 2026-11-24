# 📱 南亞數位金融生態圈：數位錢包顧客終身價值 (LTV) 資料探勘與客群分析

    ![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
    ![Jupyter Notebook](https://img.shields.io/badge/Notebook-Data.ipynb-orange?logo=jupyter)
    ![Domain](https://img.shields.io/badge/FinTech-Customer_LTV-green)

    本專案針對南亞新興市場（模擬 PayTM / Khalti 等數位錢包生態）之用戶交易資料進行深入的**資料探勘（Data
    Mining）**、**探索性數據分析 (EDA)** 與 **K-Means 機器學習分群**，旨在預測顧客終身價值 (Customer Lifetime Value,
    LTV) 並萃取具備商業落地價值的營運洞察。

    ---

    ## 📌 研究背景與商業洞見

    * **破除年齡迷思**：用戶年齡跨度 16~69 歲（平均 42.6 歲），打破「數位錢包僅年輕族群使用」之刻板印象。
    * **城鄉普惠金融差異**：農村（Rural）地區低收入用戶比例顯著，印證數位錢包推動無現金交易與普惠金融的關鍵角色。
    * **支付管道輪廓 (UPI vs. 儲值錢包)**：
      * **UPI 族群**：呈現「高頻率、小金額」特性，多用於日常民生消費。
      * **儲值錢包/信用卡族群**：交易金額較高，為平台帶來穩定的資金停留池與手續費收益。
    * **精準分群行銷策略**：依據回饋金滿意度、登入頻率與累計消費建立分群，提出針對高價值 VIP
    留存與沉睡用戶喚醒之建議。

    ---

    ## 📂 專案結構


  Digital_Wallet_LTV_Full_Research/
  ├── digital_wallet_ltv_dataset.csv   # 原始數據集（包含消費特徵、活躍度、LTV 等）
  ├── final_cluster_results.csv        # K-Means 聚類分析輸出結果
  ├── Data.ipynb                       # 完整分析工作流程（數據清洗、特徵工程、建模）
  ├── index.html                       # 視覺化研究成果報告首頁
  ├── 2index.html                      # 互動式儀表板備份
  └── README.md


    ---

    ## 🔬 特徵欄位說明

    | 欄位名稱 | 說明 |
    | :--- | :--- |
    | `Age` / `Location` | 用戶年齡與城鄉地理分佈（Urban / Semi-Urban / Rural） |
    | `Total_Transactions` | 歷史累積交易筆數 |
    | `Avg_Transaction_Value` | 平均單筆交易金額 |
    | `Total_Spent` | 累計消費總額 |
    | `Active_Days` / `Last_Transaction_Days_Ago` | 平台活躍天數與最後一次交易距今天數 |
    | `Cashback_Received` | 領取之現金回饋金額 |
    | `Customer_Satisfaction_Score` | 顧客滿意度評分 (1~10) |
    | **`LTV` (目標變數)** | 顧客預估終身價值 (Customer Lifetime Value) |

    ---

    ## 🚀 快速開始

    ### 1. 安裝環境需求
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
  2. 開啟分析 Notebook
    jupyter notebook Data.ipynb

  3. 查看視覺化成果

  直接在瀏覽器中點擊開啟 index.html 即可瀏覽研究圖表與分群報告。
