# Retina Defect Classification by Deep Learning
## 背景介紹:
此次為分辨視網膜是否正常，影像分為Normal、CNV(脈絡膜新生血管生成)、DME(黃斑部水腫)及Drusen(隱結)等四種。

CNV(脈絡膜新生血管生成): 脈絡膜是眼睛主要的血管結構層，當脈絡膜產生了不正常的新生血管，引起AMD(年齡相關性黃斑部退化)病變，視力障礙的重要因素之一。

DME(黃斑部水腫): 視網膜有豐富的血管，若血糖控制不良，會引起視網膜黃斑部微細血管病變，產生水腫情形。

Drusen(隱結): 黃斑部形成黃色的沉積物，稱為「隱結」(視網膜上小的黃色小點)。隨著隱結的形成、擴大，患者的視力會受到影響，所見物體變得扭曲或模糊，後期更會造成組織壞死。起初患者的視力只會出現部分的模糊，最終可能完全失明。


![image](https://github.com/tddwso/Retina-Defect-Classification-by-Deep-Learning/blob/main/%E5%88%86%E9%A1%9E%E7%85%A7.PNG)

## 預計完成目標:
以卷積神經網絡(Convolutional Neural Network)學習分辨視網膜四種狀況。
運用Transfer Learning(遷移式學習)，將他人訓練好的(pre-trained model)參數複製過來，當作我們模型參數，
使用的模型: VGG16，VGG 是英國牛津大學 Visual Geometry Group 的縮寫，主要貢獻是使用更多的隱藏層，大量的圖片訓練，提高準確率至90%。
## 資料集:
Train Data : 1334
## 使用環境:
Python 3.8

TensorFlow 2.3.1 
## 訓練和測試結果
最佳模型訓練準確度79% 

![image](https://github.com/tddwso/Retina/blob/main/ACC.PNG)

ROC曲線 (Receiver operating characteristic curve) & AUC (Area Under Curve)

ROC曲線會以對角線為基準，曲線下的面積(AUC)來判別ROC曲線的鑑別力，AUC數值的範圍從0到1，數值愈大，代表模型的鑑別力越好。

![image](https://github.com/tddwso/Retina/blob/main/ROC.PNG)

實際測試結果

![image](https://github.com/tddwso/Retina/blob/main/test1.PNG)

## 使用Streamlit App展示成果

![image](https://github.com/tddwso/Retina-Defect-Classification-by-Deep-Learning/blob/main/Stream%20Logo.png)

Streamlit 是一個開源Python函式庫，可以快速製作Data App。

![image](https://github.com/tddwso/Retina-Defect-Classification-by-Deep-Learning/blob/main/streamlit.png)

實作影片
https://youtu.be/MMr6gDYNouw

