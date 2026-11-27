# Computer-Vision-Course
---------------------------------------------------------------------------------------------------------
# Editor Information
 - Ph.D. Student, Ching-Hung Wang (王清弘)
 - Graduate Institute, Prospective Technology of Electrical Engineering and Computer Science
 - National Chin-Yi University of Technology (NCUT)
 - Email: chwang@gm.student.ncut.edu.tw
---------------------------------------------------------------------------------------------------------

# 電腦視覺實驗教材（基於 OpenCV 5.x）

在人工智慧技術狂飆突進的時代，電腦視覺（Computer Vision）作為機器感知真實世界的基石，是一門橫跨訊號處理、幾何數學、人工智慧與系統工程的綜合學科，其教學模式也正迎來前所未有的變革。回顧過去的電腦視覺課程，教學現場往往在「繁瑣的底層數學推導」與「零碎的語法除錯」之間掙扎，導致學生容易迷失於程式碼細節，而忽略了演算法背後的物理意義與幾何直覺；另一方面，在現代 AI 技術高速演進的背景下，許多學習者更面臨「只懂呼叫深度學習套件，卻缺乏底層影像處理直覺」，以及「演算法在實驗室表現優異，卻無法落地至真實產線」的雙重斷層。

為解決上述痛點，本實驗教材專為資訊工程學系「電腦視覺實作訓練課程（Computer Vision Practical Training Course）」量身打造，採用最新世代的 OpenCV 5.x 作為貫穿全書的核心開發框架，並將 Claude、Gemini 與 ChatGPT 三大主流生成式 AI 工具深度整合至教學與實驗流程中。我們旨在建立一種結合「AI 輔助程式開發（AI-Assisted Coding）」的現代教學模式，將學生從重複性的語法除錯中解放出來，使其能將心力專注於理解演算法的數學本質、系統架構設計與工程問題的排查。

在內容規劃上，本實驗教材依循由淺入深的螺旋式學習路徑，引領學生從最底層的數位影像本質與像素矩陣出發，紮實掌握空間與頻率域等傳統影像處理演算法的精髓；進而無縫銜接至現代深度學習視覺任務、3D 幾何空間感知與多模態基礎模型；最終更進一步跨足邊緣運算加速、MLOps 視覺系統工程化部署，以及涵蓋智慧製造、智慧醫療、智慧交通與智慧場域的端到端產業專題實戰。透過理論、AI 協作與系統落地的緊密結合，本教材期許能協助學生徹底弭平學術研究與產業應用之間的鴻溝，培養兼具底層直覺與工程落地能力的新世代電腦視覺人才。

---

## 一、 大學部課程章節總覽
本大學部實驗教材共包含 18 個核心實驗單元（CH0 – CH16），依循由淺入深的學習路徑設計，從 OpenCV 5.x 開發環境與數位影像底層結構出發，逐步涵蓋幾何變換、空間與頻率域經典演算法，最終銜接現代深度學習與高階視覺辨識任務。
* `CH0_OpenCV基礎`
* `CH0_影像繪製`
* `CH1_數位影像`
* `CH2_色彩空間`
* `CH3_幾何轉換`
* `CH4_影像數學與邏輯運算`
* `CH5_閾值處理`
* `CH6_形態學`
* `CH7_空間域濾波與降噪`
* `CH8_邊緣偵測與影像梯度`
* `CH9_輪廓分析與形狀描述`
* `CH10_頻率域濾波與正交轉換`
* `CH11_影像增強`
* `CH12_深度學習`
* `CH13_影像分類`
* `CH14_物體偵測`
* `CH15_影像分割`
* `CH16_物體追蹤`
---

## 二、 研究所課程章節總覽
本研究所實驗教材共包含六個核心進階單元與產業專題，專論探討從「三維幾何空間感知」、「神經場景表徵」、「多模態語意理解」，一路延伸至「邊緣推論加速」與「邊緣系統工程化」的前沿電腦視覺技術與產業實務。課程延續大學部 2D 影像處理與深度學習的實作基礎，引領研究生深入數學幾何推導、可微渲染原理、視覺語言模型及 MLOps 產線部署，培養獨立進行學術研究與高階視覺系統開發的完整能力。
* `CH17_相機建模、校正與雙目立體視覺`
* `CH18_多視角幾何、運動恢復結構與深度估計`
* `CH19_神經輻射場與現代 3D 場景重建`
* `CH20_視覺基礎模型與多模態整合`
* `CH21_邊緣運算與推論效能優化`
* `CH22_視覺系統部署與工程化`
* `CH23_端到端產業專題實戰`

## 二、 教材架構
本實驗教材以 OpenCV 5.x 作為貫穿核心實作工具，從最底層的像素矩陣出發，循序漸進地涵蓋經典數位影像處理、現代深度學習、3D 幾何與多模態基礎模型，最終延伸至邊緣運算加速、MLOps 系統工程化與跨領域產業專題，共計 24 個單元（CH0 – CH23）的螺旋式學習路徑，系統性劃分為以下六大教學階段

### 第一階段：基礎入門與數位影像本質（CH0 – CH2）
建立開發環境與資料結構認知，理解電腦如何「看見」並儲存視覺資訊。

* **CH0_OpenCV 基礎 & CH0_影像繪製**：熟悉 OpenCV 5.x 環境配置、基本 I/O 讀寫、事件迴圈與向量圖形繪製（線條、幾何圖形、文字標註），作為後續演算法結果視覺化的基礎。
* **CH1_數位影像**：探討取樣（Sampling）與量化（Quantization）、像素矩陣結構（NumPy 與 `cv.Mat` 的記憶體對應）、位元深度及空間解析度對影像品質的影響。
* **CH2_色彩空間**：解析人眼視覺與硬體顯示差異，實作 BGR、RGB、HSV、Lab、YCbCr 等色彩空間轉換，並應用於特定顏色物件提取與光照不變性處理。

---

### 第二階段：幾何與像素級基礎運算（CH3 – CH6）
針對單張或多張影像進行空間座標變換與像素集合邏輯操作。

* **CH3_幾何轉換**：涵蓋仿射變換（Affine Transformation：平移、旋轉、縮放、錯切）、透視變換（Perspective Transformation / Homography）與影像插值演算法（最近鄰、雙線性、雙三次插值）。
* **CH4_影像數學與邏輯運算**：實作影像加減乘除、Alpha 混合（Blending）、位元邏輯運算（AND、OR、XOR、NOT）以及 ROI（感興趣區域）遮罩（Masking）合成技術。
* **CH5_閾值處理**：從全域固定閾值（Global Thresholding）、Otsu 大津演算法（自動尋找最佳雙峰閾值），進階至自適應局部閾值（Adaptive Thresholding）以克服不均勻光照問題。
* **CH6_形態學**：基於集合論的二值與灰階影像處理，包含侵蝕（Erosion）、膨脹（Dilation）、開運算（Opening）、閉運算（Closing）、梯度(Gradient)、頂帽（Top-hat）與黑帽（Black-hat）運算，用於去除雜訊與修補物件輪廓。

---

### 第三階段：從空間域轉換至頻率域（CH7 – CH11）
進入經典影像處理核心，學習濾波降噪、邊緣輪廓分析與頻譜轉換。

* **CH7_空間域濾波與降噪**：探討卷積（Convolution）與相關（Correlation）運算，實作線性濾波（均值、高斯模糊）與非線性濾波（中值濾波去除椒鹽雜訊、雙邊濾波 （Bilateral Filter ）保留邊緣細節）。
* **CH8_邊緣偵測與影像梯度**：計算一階與二階空間導數，實作 Sobel、Scharr、Laplacian 運算子，並深入拆解 Canny 邊緣偵測器的多階段流程（高斯平滑、梯度計算、非極大值抑制（NMS）、雙閾值滯後追蹤）。
* **CH9_輪廓分析與形狀描述**：提取連通區域與階層輪廓，計算幾何特徵（面積、周長、質心、外接矩形、最小外接圓、凸包 Convex Hull）以及影像矩（Image Moments 與 Hu 不變矩），以進行形狀比對。
* **CH10_頻率域濾波與正交轉換**：透過二維離散傅立葉轉換（2D DFT / FFT）將影像從空間域轉換至頻率域，設計低通、高通、帶通與帶阻濾波器（處理週期性雜訊），並介紹離散餘弦轉換（DCT）。
* **CH11_影像增強**：改善影像視覺對比度與動態範圍，包含伽瑪校正（Gamma Correction）、直方圖等化（Histogram Equalization）以及限制對比度自適應直方圖等化（CLAHE）。

---

### 第四階段：深度學習與高階視覺任務（CH12 – CH16）
銜接現代 AI 視覺辨識技術，利用 OpenCV 5.x 整合 ONNX 與 PyTorch 預訓練模型，建構高效能的深度學習推論流程，全面掌握現代電腦視覺的核心應用。

* **CH12_深度學習**：掌握 OpenCV `dnn` 模組架構，學習載入 ONNX、PyTorch 匯出模型，進行影像前處理（`blobFromImage`）、硬體後端加速（CUDA）與推論效能優化。
* **CH13_影像分類**：針對醫學影像（如 X 光、眼底鏡、病理切片）低對比度與背景雜訊多的特性，透過 ROI 自動裁切與 CLAHE 對比度增強，並將其封裝至醫療深度學習框架 MONAI 中進行模型訓練，最後透過臨床評估指標（混淆矩陣、敏感度/特異度、ROC/AUC），完成端到端的智慧醫療分類實驗。
* **CH14_物體偵測**：實作基於錨點（Anchor-based）與無錨點（Anchor-free）的現代偵測架構（如 YOLO 系列、DETR 系列），並實作非極大值抑制（NMS）與邊界框視覺化。
* **CH15_影像分割**：從傳統分水嶺演算法（Watershed）與 GrabCut 互動式前景提取，過渡到語意分割（Semantic Segmentation）與實例分割（Instance Segmentation）的像素級分割實作。
* **CH16_物體追蹤**：結合傳統光流法（Optical Flow，如 Lucas-Kanade）、卡爾曼濾波器（Kalman Filter）的狀態預測，以及現代多目標追蹤（MOT，如 ByteTrack / DeepSORT 概念與 OpenCV Tracker API），實現動態視訊追蹤。

---

### 第五階段：從 3D 幾何視覺到多模態模型（CH17 – CH20）
從二維平面跨足三維空間感知，完整串聯傳統多視角幾何、學習式深度估計與神經場景表徵，並進一步銜接現代視覺基礎模型與跨模態語意理解，建立兼具空間幾何精度與開放式語意泛化能力的進階視覺知識體系。

* **CH17_相機建模、校正與雙目立體視覺**：探討三維幾何表徵、針孔相機模型、內外參數矩陣與鏡頭畸變校正（張正友校正法）；實作特徵點匹配（ORB / SIFT）、單應性變換（Homography）全景影像拼接，以及基於極線幾何（Epipolar Geometry）的雙目立體視覺（Stereo Vision）視差圖與深度估計。
* **CH18_多視角幾何、運動恢復結構與單目深度估計**：由雙目視覺擴展至多視角幾何與學習式 3D 感知，涵蓋單視角量測（Single View Metrology）與運動恢復結構（Structure from Motion, SfM）的稀疏 3D 點雲重建；並導入深度學習深度估計方法（如單目與多視角深度估計），突破傳統立體視覺對硬體基線與表面紋理的限制。
* **CH19_神經輻射場與現代 3D 場景重建**：作為傳統幾何與現代神經表徵的橋樑，探討如何透過可微渲染技術重構三維空間。內容涵蓋神經輻射場（NeRF）的體積渲染原理、3D 高斯潑濺（3D Gaussian Splatting）即時新視角合成（Novel View Synthesis），以及 3D 點雲配準與場景視覺化實作。
* **CH20_視覺基礎模型與多模態整合**：從幾何重建邁向跨模態語意理解，介紹視覺表徵學習與圖文對齊機制（如 CLIP 概念），並學習將 OpenCV 影像前後處理與現代視覺基礎模型（Vision Foundation Models）無縫串接。實作零樣本萬物分割（SAM 系列）、開放詞彙物體偵測（Open-Vocabulary Detection）與視覺語言模型（VLM），透過文字提示（Prompt）建構自動化影像理解與半自動標註管線。

---

### 第六階段: 視覺系統部署與工程化 （CH21 – CH22）
跨越實驗室演算法驗證與實際產線落地之間的效能與工程鴻溝，從底層異質硬體加速到雲端原生 MLOps 部署，全面掌握產業級 AI 視覺系統的開發與維運實務。整合前五階段的傳統影像處理、深度學習推論、3D 視覺與邊緣部署技術，針對四大主流產業場景，完成從需求定義、演算法串接、效能調校到介面封裝的端到端（End-to-End）專案開發。

* **CH21_邊緣運算與推論效能優化**：聚焦於電腦視覺模型在邊緣端落地時所面臨的即時性與低延遲挑戰，突破硬體算力與記憶體瓶頸。課程涵蓋低位元模型量化技術（FP16 / INT8 / INT4），並深入整合 ONNX Runtime、TensorRT 與 TFLite 等跨硬體推論加速引擎，充分發揮 CPU、GPU 與 NPU 的異質運算效能；同時透過實作多執行緒非同步視訊串流架構與記憶體零拷貝（Zero-Copy）效能調校，全面消除 I/O 等待延遲，打造兼顧辨識精度與高幀率（FPS）的即時推論核心。
* **CH22_視覺系統部署與工程化**：聚焦於從「演算法原型」邁向「正式產線系統」的工程實務，完成 AI 視覺落地的最後一哩路。課程從大規模運算切入，涵蓋分散式資料處理與平行訓練（Ray / Spark），並透過動態批次處理與專用推論伺服器（如 Triton），建構高併發、高吞吐的微服務架構；同時導入 Docker、Kubernetes、Terraform 與 CI/CD 自動化管線，整合資料版本控管、GPU 資源排程、異常容錯與線上監控，確保視覺服務具備高穩定性、可重現性與擴展能力。
* **CH23_端到端產業專題實戰（Capstone Project）**：綜合運用傳統影像處理、深度學習與部署技術，完成完整系統開發（如智慧製造 AOI 瑕疵檢測、智慧交通即時車流與車牌辨識，或醫療影像輔助判讀系統），涵蓋 API 服務封裝、例外容錯處理與即時監控視覺化。

---

## 三、 實驗單元編排規範

為確保各章節檔案（建議採用 Jupyter Notebook `.ipynb` 格式）具備高度一致性與教學成效，每個實驗單元皆遵循以下標準結構：

| 單元區塊 | 教學目標與內容規範 |
| :--- | :--- |
| **1. 實驗目標 (Objectives)** | 條列本單元結束後學生應掌握的數學概念與 OpenCV 函式庫操作能力。 |
| **2. 核心理論與數學模型 (Theory)** | 精簡扼要推導核心公式（對照參考書目章節），搭配訊號與矩陣示意說明。 |
| **3. OpenCV 5.x 核心 API 解析** | 列出關鍵函式簽章（Signature）、參數意義、資料型別限制（如 `uint8` 與 `float32` 轉換陷阱）及版本更新注意事項。 |
| **4. 漸進式實作範例 (Guided Lab)** | 提供完整可執行的 Python 程式碼，包含標準測試影像載入、演算法執行與並列對比視覺化（Matplotlib / OpenCV GUI）。 |
| **5. 動手挑戰與參數調校 (Challenges)** | 設計 2–3 個開放式實作任務（例如：在強雜訊下調整 Canny 雙閾值，或結合形態學解決黏連物體計數），培養解決實際問題的能力。 |

---

## 四、 教學環境配置建議

* **程式語言**：Python 3.10 或以上版本
* **核心套件**：
  * `opencv-python` / `opencv-contrib-python` (5.x 版本)
  * `numpy`
  * `matplotlib`
  * `scipy`
  * `onnxruntime`
* **開發工具**：
  * `JupyterLab`
  * `VS Code`
  * `PyCharm`

---

## 五、 實用與參考資源

### 線上官方資源
* 📖 [OpenCV 5.0 官方文檔](https://docs.opencv.org/5.0)

### 參考書目
1. Rafael C. Gonzalez, Richard E. Woods (2017). *Digital Image Processing* (4th ed.). Pearson FT Press.
2. Davies, E. R. (2017). *Computer Vision: Principles, Algorithms, Applications, Learning* (5th ed.). Academic Press.
3. Tyler, Christopher W. (2019). *Computer Vision: From Surfaces to 3D Objects*. CRC Press.
4. Szeliski, R. (2022). *Computer Vision: Algorithms and Applications* (2nd ed.). Springer.
   - https://link.springer.com/book/10.1007/978-3-030-34372-9
6. Zhang, Y. J. (2022). *2-D Computer Vision: Principles, Algorithms and Applications*. World Scientific Pub.
7. Zhang, Y. J. (2023). *3-D Computer Vision: Principles, Algorithms and Applications*. Springer.
   - https://link.springer.com/book/10.1007/978-981-19-7580-6
8. Torralba, A., Isola, P., & Freeman, W. T. (2024). *Foundations of Computer Vision*. MIT Press.
   - https://visionbook.mit.edu/
10. Nixon, M., & Aguado, A. S. (2025). *Feature Extraction and Image Processing for Computer Vision* (5th ed.). Academic Press.
11. Machine Learning Systems
    - https://github.com/harvard-edge/cs249r_book
12. Vijay Janapa Reddi (2026). *Introduction to Machine Learning Systems*. The MIT Press
    - https://mlsysbook.ai/vol1/
13. Vijay Janapa Reddi (2027). *Scaling Machine Learning Systems*. The MIT Press
    -  https://mlsysbook.ai/vol2/


