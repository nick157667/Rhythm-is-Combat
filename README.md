# Rhythm-is-Combat
[demo影片](https://youtu.be/swUgUA5DlT8?si=62gDe4qnIsStRrcp)



# 組員
張育銓、周柏儒

# 指導教授
李同益 講座教授


# 專題簡介
《Rhythm is Combat》 是一款結合 AI 音樂生成與節奏判定射擊系統的 3D 第一人稱射擊遊戲。遊戲透過 Stable Audio 1.0 根據玩家輸入提示詞自動產生音樂，並以 BurstFFT 分析音樂節奏資訊，生成節奏圖譜（beatmap）。敵人會正常出現，但玩家必須跟著節奏射擊，才能成功造成傷害或得分。 

# 遊戲架構圖
<img width="1269" height="479" alt="遊戲架構圖" src="https://github.com/user-attachments/assets/7f7f10a0-bf97-4966-853e-6918ef7687db" />

# 遊戲核心技術

## 基於擴散模型的音樂生成
玩家輸入的提示詞先由 CLIP 模型轉換為語意向量，作為條件輸入（conditioning）。生成過程中，初始化的 latent 音訊張量與提示詞向量一同傳入 dpmpp_3m_sde 取樣器，以連續擴散方式進行100次的去噪推理，最終輸出經 VAE 解碼為真實音訊波形，並儲存為 .flac 檔

<img width="916" height="205" alt="擴散模型" src="https://github.com/user-attachments/assets/c8f09bde-8aed-4e57-b780-6d3e83231bf2" />

## ComfyUI工作流
<img width="1599" height="564" alt="ComfyUI" src="https://github.com/user-attachments/assets/05c719c1-32b3-46fa-b607-5d05a5b888d1" />



## 分析音樂


## 避障行為 


