# 第二屆機器學習百日馬拉松 2nd-ML100Days

![Marathon Flow](/marathon.png)

## 資料清理數據前處理

[[Day1]資料介紹與評估資料](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_001_HW.ipynb)

[[Day2]讀取資料EDA: Data summary](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_002_HW.ipynb)

[[Day3]如何新建一個 dataframe?如何讀取其他資料? (非 csv 的資料)](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_003_HW.ipynb)

[[Day4]EDA: 欄位的資料類型介紹及處理](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_004_HW.ipynb)

	- 拿到資料的第一步，通常就是看我們有什麼，觀察有什麼欄位，這些欄位代表什麼意義、以什麼樣的資料類型來儲存
	- 資料原來是字串/類別的話，如果要做進⼀步的分析時（如訓練模型），⼀般需要轉為數值的資料類型，轉換的⽅式通常有兩種
		• Label encoding：使用時機通常是該資料的不同類別是有序的，例如該資料是年齡分組，類別有⼩孩、年輕⼈、老人，表⽰示為 0, 1, 2 是合理理的，因為年齡上老人 > 年輕人 > 小孩
		• One Hot encoding：使用時機通常是該資料的不同類別是無序的，例如國家

[[Day5]EDA資料分佈](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_005_HW.ipynb)

## 資料科學特徵工程技術

[[Day23]類別型特徵 - 均值編碼](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_023_HW.ipynb)  

[[Day24]類別型特徵 - 其他進階處理理](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_024_HW.ipynb)  

[[Day25]時間型特徵](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_025_HW.ipynb) 

[[Day26]特徵組合 - 數值與數值組合](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_026_HW.ipynb)  

	- 數值與數值的特徵組合，最關鍵的部分是領域知識
	- 機器學習的關鍵是特徵工程，當然其餘部分仍然很重要，但是各部分都熟悉之後，最有效提升模型預測⼒的部分就是特徵工程

[[Day27]特徵組合 - 類別與數值組合](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_027_HW.ipynb)  

	- 類別特徵與數值特徵，可以使⽤用群聚編碼組合出新的特徵
	- 群聚編碼最常使⽤用的運算是 mean, 除此之外還有median、mode、max、min、count等統計量量可以使⽤
	- 用群聚編碼與之前的均值編碼最主要的差異異，⼀個是特徵彼此之間與特徵⽬目標值之間的差異異，另⼀個最⼤的差異是 : 
	群聚編碼因為與目標值無關，因此不容易Overfitting，也因此比均值編碼使⽤頻率高得多


[[Day28]特徵選擇](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_028_HW.ipynb)  

	- 相對於特徵組合在增加特徵，特徵選擇就是在減少特徵
	- 特徵選擇主要包含：過濾法(Filter)、包裝法(Wrapper)與嵌入法(Embedded)
	- 特徵選擇中，計算時間較長，但是能排除共線性且比較穩定的方式是梯度提升樹嵌入法

[[Day29]特徵評估](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_029_HW.ipynb)  

	- 樹狀狀模型的特徵重要性，可以分為分⽀次數、特徵覆蓋度、損失函數降低量三種
	- sklearn 樹狀狀模型與 Xgboost 的特徵重要性，最大差異就是在sklearn 只有精準度最低的「分⽀支次數」
	- 特徵重要性本身的重要性，是在於本⾝身是增刪特徵的重要判定準則，在領域知識不⾜時，成為改善模型的最⼤幫手

[[Day30]分類型特徵優化 - 葉編碼](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_030_HW.ipynb)  

	- 多個分類預測結果，需要先將機率到推回對應數值，相加後再由sigmoid函數算回機率，類似邏輯斯回歸的算法
	- 葉編碼的目的是重新標記資料，以擬合後的樹狀模型分歧條件，將資料離散化，這樣比人為寫作的判斷條件更精確，更符合資料的分佈情形
	- 葉編碼完後，因為特徵數量較多，通常搭配邏輯斯回歸或者分解機做預測，其他模型較不適合

## 機器學習基礎模型建立

[[Day31]機器學習概論](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_031_HW.ipynb)

[[Day32]機器學習-流程與步驟](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_032_HW.ipynb)

[[Day33]機器如何學習？](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_033_HW.ipynb)

[[Day34]訓練/測試集切分的概念](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_034_HW.ipynb)

[[Day35]Regression vs. Classification](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_035_HW.ipynb)

[[Day36]評估指標選定](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_036_HW.ipynb)

	- 評估指標選擇
		- 回歸問題：R-square
		- 類問題(二元)：AUC
		- 想特別觀察哪一類：F1-Score
		- 分類問題(多元)：top-k 
	- AUC 計算時填入每個樣本預測機率
	- F1-Score則是每個以分類結果機率>0.5視為1

[[Day37]Regression 模型](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_037_HW.ipynb)

[[Day38]Regression 模型-程式碼](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_038_HW.ipynb)

[[Day39]LASSO, Ridge Regression](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_039_HW.ipynb)

	- 為避免overfitting，我們可以加入正規化，目標函數＝損失函數＋正規化
	- 正規化可以懲罰模型的複雜度，當模型越複雜期值越大
	- LASSO＝Linear Regression + L1
	- Ridge＝Linear Regression + L2
	- LASSO之所以可以當作特徵選取的工具，是因為他是以參數稀疏化來做訓練的，因此某些特徵最後權重會變成0，達成特徵選取之功用

[[Day40]LASSO, Ridge Regression-程式碼](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_040_HW.ipynb)

[[Day41]決策樹](https://github.com/yzmsp7/2nd-ML100Days/blob/master/homework/Day_041_HW.ipynb)

	- 透過一系列的是非問題，幫助我們將資料進行切分
	- 衡量資料相似程度可以用Gini&Entropy
	- 我們可以從構建樹的過程中，透過feature被用來切分的次數來判斷哪些feature是相對有用的



## 機器學習調整參數

## 非監督式機器學習

## 初探深度學習 - 使用Keras

## 深度學習應用卷積神經網路
