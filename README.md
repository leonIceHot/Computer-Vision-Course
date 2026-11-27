# Computer-Vision-Course
---------------------------------------------------------------------------------------------------------
# Editor Information
 - Ph.D. Student, Ching-Hung Wang (王清弘)
 - Graduate Institute, Prospective Technology of Electrical Engineering and Computer Science
 - National Chin-Yi University of Technology (NCUT)
 - Email: chwang@gm.student.ncut.edu.tw
---------------------------------------------------------------------------------------------------------

# 電腦視覺實驗教材（基於 OpenCV 5.x）

在人工智慧技術狂飆突進的時代，電腦視覺（Computer Vision）作為機器感知真實世界的基石，其教學模式正迎來前所未有的變革。過去的大學部電腦視覺課程，往往在「繁瑣的底層數學推導」與「零碎的語法除錯」之間掙扎，導致學生容易迷失於程式碼的細節，而忽略了演算法背後的物理意義與幾何直覺。

本教材專為資工系 「電腦視覺實作訓練課程（Computer Vision Practical Training Course）」 量身打造，採用最新世代的 OpenCV 5.x 作為核心開發框架，並將 Claude、Gemini 與 ChatGPT 三大主流生成式 AI 工具深度整合至教學流程中。我們旨在建立一種結合 「AI 輔助程式開發（AI-Assisted Coding）的現代教學模式，引領學生從數位影像的底層原理出發，掌握傳統影像處理演算法的精髓，並無縫銜接至現代深度學習的視覺應用。

---

## 一、 課程章節總覽

本教材大學部共包含 18 個核心實驗單元，依循由淺入深的學習路徑設計：
* `CH0_影像繪製`
* `CH0_OpenCV基礎`
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
* `CH13_醫學影像分類`
* `CH14_物體偵測`
* `CH15_影像分割`
* `CH16_物體追蹤`

---

## 二、 教材架構與四大學習階段

本教材結合經典電腦視覺理論與 OpenCV 5.x 的最新 API 特性（包含強化的 `cv.dnn` 模組、現代化 G-API 管線加速，以及更完善的型別與硬體抽象支援），將所有章節劃分為以下四大教學階段：

### 第一階段：基礎入門與數位影像本質（CH0 – CH2）
建立開發環境與資料結構認知，理解電腦如何「看見」並儲存視覺資訊。

* **CH0_影像繪製 & CH0_OpenCV 基礎**：熟悉 OpenCV 5.x 環境配置、基本 I/O 讀寫、事件迴圈與向量圖形繪製（線條、幾何圖形、文字標註），作為後續演算法結果視覺化的基礎。
* **CH1_數位影像**：探討取樣（Sampling）與量化（Quantization）、像素矩陣結構（NumPy 與 `cv.Mat` 的記憶體對應）、位元深度及空間解析度對影像品質的影響。
* **CH2_色彩空間**：解析人眼視覺與硬體顯示差異，實作 BGR、RGB、HSV、Lab、YCbCr 等色彩空間轉換，並應用於特定顏色物件提取與光照不變性處理。

### 第二階段：幾何與像素級基礎運算（CH3 – CH6）
針對單張或多張影像進行空間座標變換與像素集合邏輯操作。

* **CH3_幾何轉換**：涵蓋仿射變換（Affine Transformation：平移、旋轉、縮放、錯切）、透視變換（Perspective Transformation / Homography）與影像插值演算法（最近鄰、雙線性、雙三次插值）。
* **CH4_影像數學與邏輯運算**：實作影像加減乘除、Alpha 混合（Blending）、位元邏輯運算（AND、OR、XOR、NOT）以及 ROI（感興趣區域）遮罩（Masking）合成技術。
* **CH5_閾值處理**：從全域固定閾值（Global Thresholding）、Otsu 大津演算法（自動尋找最佳雙峰閾值），進階至自適應局部閾值（Adaptive Thresholding）以克服不均勻光照問題。
* **CH6_形態學**：基於集合論的二值與灰階影像處理，包含侵蝕（Erosion）、膨脹（Dilation）、開運算（Opening）、閉運算（Closing）、梯度(Gradient)、頂帽（Top-hat）與黑帽（Black-hat）運算，用於去除雜訊與修補物件輪廓。

### 第三階段：從空間域轉換至頻率域（CH7 – CH11）
進入經典影像處理核心，學習濾波降噪、邊緣輪廓分析與頻譜轉換。

* **CH7_空間域濾波與降噪**：探討卷積（Convolution）與相關（Correlation）運算，實作線性濾波（均值、高斯模糊）與非線性濾波（中值濾波去除椒鹽雜訊、雙邊濾波 （Bilateral Filter ）保留邊緣細節）。
* **CH8_邊緣偵測與影像梯度**：計算一階與二階空間導數，實作 Sobel、Scharr、Laplacian 運算子，並深入拆解 Canny 邊緣偵測器的多階段流程（高斯平滑、梯度計算、非極大值抑制（NMS）、雙閾值滯後追蹤）。
* **CH9_輪廓分析與形狀描述**：提取連通區域與階層輪廓，計算幾何特徵（面積、周長、質心、外接矩形、最小外接圓、凸包 Convex Hull）以及影像矩（Image Moments 與 Hu 不變矩），以進行形狀比對。
* **CH10_頻率域濾波與正交轉換**：透過二維離散傅立葉轉換（2D DFT / FFT）將影像從空間域轉換至頻率域，設計低通、高通、帶通與帶阻濾波器（處理週期性雜訊），並介紹離散餘弦轉換（DCT）。
* **CH11_影像增強**：改善影像視覺對比度與動態範圍，包含伽瑪校正（Gamma Correction）、直方圖等化（Histogram Equalization）以及限制對比度自適應直方圖等化（CLAHE）。

### 第四階段：深度學習與高階視覺任務（CH12 – CH16）
銜接現代 AI 視覺辨識技術，利用 OpenCV 5.x 整合 ONNX 與 PyTorch 預訓練模型，建構高效能的深度學習推論流程，全面掌握現代電腦視覺的核心應用。

* **CH12_深度學習**：掌握 OpenCV `dnn` 模組架構，學習載入 ONNX、PyTorch 匯出模型，進行影像前處理（`blobFromImage`）、硬體後端加速（CUDA）與推論效能優化。
* **CH13_影像分類**：針對醫學影像（如 X 光、眼底鏡、病理切片）低對比度與背景雜訊多的特性，透過 ROI 自動裁切與 CLAHE 對比度增強，並將其封裝至醫療深度學習框架 MONAI 中進行模型訓練，最後透過臨床評估指標（混淆矩陣、敏感度/特異度、ROC/AUC），完成端到端的智慧醫療分類實驗。
* **CH14_物體偵測**：實作基於錨點（Anchor-based）與無錨點（Anchor-free）的現代偵測架構（如 YOLO 系列、DETR 系列），並實作非極大值抑制（NMS）與邊界框視覺化。
* **CH15_影像分割**：從傳統分水嶺演算法（Watershed）與 GrabCut 互動式前景提取，過渡到語意分割（Semantic Segmentation）與實例分割（Instance Segmentation）的像素級分割實作。
* **CH16_物體追蹤**：結合傳統光流法（Optical Flow，如 Lucas-Kanade）、卡爾曼濾波器（Kalman Filter）的狀態預測，以及現代多目標追蹤（MOT，如 ByteTrack / DeepSORT 概念與 OpenCV Tracker API），實現動態視訊追蹤。

### 第五階段：3D 幾何視覺、多模態模型與系統部署（CH17 – CH20）
從二維平面跨足三維空間感知，並整合最新多模態模型與邊緣運算加速技術，完成從演算法驗證到實際產線落地的最後一哩路。

* **CH17_相機校正與 3D 立體視覺**：探討針孔相機模型、內外參數矩陣與鏡頭畸變校正（張正友校正法），並實作特徵點匹配（ORB / SIFT）、全景影像拼接（Image Stitching）與雙目立體視覺（Stereo Vision）視差圖及深度估計。
* **CH18_視覺基礎模型與多模態整合**：結合 OpenCV 影像前處理與現代大型視覺模型，實作零樣本萬物分割（SAM 系列）、開放詞彙物體偵測（Open-Vocabulary Detection）以及視覺語言模型（VLM）的自動化影像理解與標註流程。
* **CH19_邊緣運算與推論效能優化**：針對即時性與低延遲需求，學習模型量化（FP16 / INT8）、ONNX Runtime / TensorRT / OpenVINO 跨硬體加速引擎整合，並實作多執行緒非同步視訊串流（RTSP / GStreamer）與記憶體零拷貝（Zero-Copy）效能調校。
* **CH20_視覺系統部署與工程化**：學習將視覺演算法封裝為可上線的微服務（如 FastAPI），實作 Docker 容器化環境建置、GPU 資源排程、異常容錯機制與推論日誌監控，完成進入產線前的最後一哩路。

### 第六階段：跨領域產業專題實戰（CH21 – CH25）
整合前五階段的傳統影像處理、深度學習推論、3D 視覺與邊緣部署技術，針對四大主流產業場景，完成從需求定義、演算法串接、效能調校到介面封裝的端到端（End-to-End）專案開發。

* **CH21_端到端產業專題實戰（Capstone Project）**：綜合運用傳統影像處理、深度學習與部署技術，完成完整系統開發（如智慧製造 AOI 瑕疵檢測、智慧交通即時車流與車牌辨識，或醫療影像輔助判讀系統），涵蓋 API 服務封裝、例外容錯處理與即時監控視覺化。
* **CH22_智慧製造：AOI 表面瑕疵檢測與精密尺寸量測**
結合相機畸變校正（CH17）、形態學與邊緣輪廓分析（CH6、CH8、CH9）進行次像素級（Sub-pixel）幾何尺寸量測；並串接語意分割或異常檢測模型（CH15），針對金屬刮痕、PCB 焊點缺陷等微米級瑕疵建立高檢出率、低過殺率的自動光學檢測產線原型。
* **CH23_智慧醫療：醫學影像病灶分割與輔助判讀系統**
延伸 CH13 的醫療影像架構，整合 CLAHE 對比度增強（CH11）、MONAI 深度學習框架與 SAM 互動式分割（CH18），針對肺部 X 光、腦部 MRI 或眼底鏡影像進行病灶自動圈選與面積量化，並輸出符合臨床評估標準（Dice Score、Sensitivity/Specificity、熱力圖可視化）的輔助診斷報告介面。
* **CH24_智慧交通：即時多目標車流分析與車牌辨識（ANPR）**
透過透視變換（CH3）建立鳥瞰視角估算車速，串接 YOLO 物體偵測（CH14）、ByteTrack 多目標追蹤（CH16）與 OCR 字元辨識，搭配 RTSP 多執行緒串流與 TensorRT / OpenVINO 加速（CH19），實現高幀率（FPS）的即時車流量統計、越線違規偵測與車牌自動建檔系統。
* **CH25_智慧場域與互動應用：多模態空間感知與邊緣部署**
結合開放詞彙物體偵測、視覺語言模型（VLM）（CH18）與立體深度估計（CH17），打造具備語意理解與距離感知的智慧監控或零售分析系統（如異常行為預警、貨架缺貨偵測與熱區軌跡分析），並完成 Docker 容器化封裝、Web API 串接與長期運作的例外容錯監控。

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
* **開發介面**：
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
5. Zhang, Y. J. (2022). *2-D Computer Vision: Principles, Algorithms and Applications*. World Scientific Pub.
6. Zhang, Y. J. (2023). *3-D Computer Vision: Principles, Algorithms and Applications*. Springer.
7. Torralba, A., Isola, P., & Freeman, W. T. (2024). *Foundations of Computer Vision*. MIT Press.
8. Nixon, M., & Aguado, A. S. (2025). *Feature Extraction and Image Processing for Computer Vision* (5th ed.). Academic Press.
